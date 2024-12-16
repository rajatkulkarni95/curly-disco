Hi, yeah **sure** - I'm using ReactJS, and I handle auto saving in two ways...

I created a debounce hook (that I wrote about here <https://www.codemzy.com/blog/reactjs-debounce-hook>) so I can control how often functions run, and also an autosave hook (that I wrote about here <https://www.codemzy.com/blog/autosave-reactjs-with-setinterval>) to run a function (like saving) on an interval. I use both these hooks for autosaving.

To start with I keep a track of changes in the editor...

```
// debounce function to set changes to reduce calls to getJSON
const debounceChanges = useDebounce(function(editor) {
  toSave.current = editor.getJSON();
  debounceSave(); // trigger save for any changes
}, 250, []); // every .25 of a second max

// in the editor
 //...
            editor.on('update', ({ editor }) => {
                debounceChanges(editor); // run change through debounce for performance
            });
  //...
```

Then save after a user pauses for more than 7 seconds, this is how I use the `useDebounce` hook to do that...

```
// debounce save after no activity in editor
const debounceSave = useDebounce(function() {
  handleSave();
}, 7 * 1000, []); // every 7 seconds max
```

And if they don't take a pause, (e.g. they are continuously typing for more than a minute), I'll also autosave with the `useAutosave` hook...

```
useAutosave(() => {
  // run save if changes and not already saving
  if (isChanges && !isSaving) {
    handleSave();
  }
}, 60 * 1000, [id]); // autosave every minute
```

Hope that helps! I'll try and write this whole thing up with more detail on my blog.