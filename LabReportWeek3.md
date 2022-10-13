# Week 3 Lab Report
Casey Loftus
A16860039

## Search Engine Code
```
public String handleRequest(URI url) {
        if (url.getPath().equals("/")){
            return String.format("No Query!");
        } else if (url.getPath().contains("/add")){
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                items.add(parameters[1]);
                String itemList = String.join(", ", items);
                return String.format("All Words: %s", itemList);
            }
        } else if (url.getPath().contains("/search")){
            ArrayList<String> results = new ArrayList<String>();
            String[] parameters = url.getQuery().split("=");
            String search = parameters[1];
            for(int j = 0; j < items.size(); j += 1){
                if(items.get(j).contains(search)){
                    results.add(items.get(j));
                }
            }
            String resultList = String.join(", ", results);
            return String.format("Search Results: %s", resultList);
        }
        
        else {
            return String.format("error");
        }
```

## Example Add 
![](https://user-images.githubusercontent.com/114450184/195703120-e4af8016-f170-4dfe-891d-40b4f3b630cc.png)

* When I changed the URL by adding the additional search parameters, this accesses the handleRequest method in my code. 
* In this case, since the updated URL contains the add parameter, it simply parses the query string for he "=" and adds everything to the right of the "=" to the items ArrayList. It then returns the formatted items array.

## Example Search
![](https://user-images.githubusercontent.com/114450184/195703092-62989bf3-95a9-4c32-bf46-a18e7faff65f.png)
* The same methods are accessed (handleRequest).
* Since the path in this case is the search path, a new array is created.
* The method then parses the query string for the search query, and iterates through the item array, adding whichever elements contain the search query to the results array.
* Finally, it returns a formatted results array. 
## Example Remove
![](https://user-images.githubusercontent.com/114450184/195707673-73f5c0c3-63e2-4835-852e-612c6b98b40a.png)
* I also added a remove feature that allows you to remove elements from the list array.
* It works the same as add, except responds with an error when the search query is not contained in the item list.

## Reverse Method Failure Inducing Input
![](https://user-images.githubusercontent.com/114450184/195709512-7df482be-214d-447c-a7be-f9a5cc91a05e.png)

## Reverse Method Symptom
![](https://user-images.githubusercontent.com/114450184/195709756-b50c700e-df90-4ce5-bdd0-9d9a86a4137e.png)

## The Bug
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```
## Connection
* The bug causes this symptom because it changes the original array to an array of zeros, then returns this original array. 
* Thus, the first element will always be zero, as in the symptom. 

## Merge Method Failure Inducing Input
![](https://user-images.githubusercontent.com/114450184/195715885-82113749-79c2-4b48-abfe-4d25542aab0e.png)

## Merge Method Symptom
![](https://user-images.githubusercontent.com/114450184/195715927-eddf7b81-3954-45ba-a52d-5f484e207665.png)

## Merge Method Bug
![](https://user-images.githubusercontent.com/114450184/195715994-cce6fe2a-9be3-4f74-a063-bf739023f6de.png)

## Connection
* The out of heap space error usually suggests a loop error that causes it to go on infinitely. This is exactly the case in this example, as in the code bug this while loop proceeds infinitely, as the code iterates the wrong index leading the initial condition to always be true. 