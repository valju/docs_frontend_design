1. You are adding code to your old frontend project (based on idea-short-demo = the given solution).

(This task is meant to make the real add category feature easier to do! As some steps are skipped)

1. Add a ajax service called addCategory, that will get a category object and try to add it to the backend. It returns the id of the added category if success and null if failure.
Now you naturally have to add the 'body' for the request, and as value have that JavaScrip category object be stringified/serialized as JSON text. And the method is naturally also _not_ 'GET'.

1. Then add one Link to the bottom of the CategoryListView, taking to the AddRandomCategoryView component. 

1. If clicked, while coming to the View, generate a random category object to be the state of this view. name = "Category nnn" where nnn is a number between 100 and 999. Budget between 10 and 9999 and
isActive is randomized between true and false (e.g. based on integer from 0 to 1).

1. Math.random() gives value between [0, 1[ meaning getting close, but under 1  (0.9999999998 or something). On first course you had task to write your randomizer from 'from' to 'to'. You can refresh your memory and write it again. Hints: first calculate the scale, then scale, then shift.

1. Randomize that object in the useEffect. Put that randomized object to state. Then have a button that will send the randomized
object to backend and print some notification on screen (you
can create a result state fraction for success or failure message,
with initial value '', nothing to show)

1. If randomizing etc. successful, empty the state of this view,
provide link to CategoryListView, or do navigation programmatically.  