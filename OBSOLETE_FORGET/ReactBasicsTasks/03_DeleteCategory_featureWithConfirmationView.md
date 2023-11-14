1. You are adding code to your old frontend project (based on idea-short-demo = the given solution).

1. Add a ajax service called e.g. deleteCategoryByCategoryId, that will get a categoryId and try to execute the delete in backend. It returns true if success and false if failure.

1. Then add an "X" button to your CategoryListView, to the CategoryListItem component. 

1. If clicked, the 'Link hiding behind the button' takes to a new view, where the details of Category are shown and you are asked for confirmation of the delete. 

1. If so, navigate back to CategoryListView (First you can do this with a Link, later you could improve it by doing it programmatically)

1. Navigating back to CategoryListView will cause useEffect run again and thus the new category list refreshed from backend. (If using confirmation dialog, we would need to refresh the list of categories by our code)  