Create a front-end application allowing a user to paste a JSON formatted in a specific way (see Input) and display the cleaned version (see Ouput).

Keep track of the amount of hours you spend on each part of this project and send them with your submission to bruno@metromerce.com.

# Step 1

The first step focuses only on the front-end side. 

- Create a JavaScript application using React (and any other library/tool you want/need).
- The application must have an editable field where the user can paste a formatted JSON (Input).
- The application must show a non-editable field displaying the updated JSON (Output).
- The application must have automated tests.
- [Here's an example of the UI](https://docs.google.com/drawings/d/15kQtFSQjNA8LVpWf1r7t9m7RPaa7G9bp0G7ZT_6VMco/edit?usp=sharing) (feel free to ignore it and do your own if you can do something better, this is just to give you a better idea of what's expected).
- (Bonus) Show off your CSS skills by making it look good.

# Step 2

This second step focuses on communication with an external API.

- Use the [GitHub API](https://developer.github.com/v3/repos/#list-all-public-repositories) to list all public repositories.
- Show 10 repositories in a table with all the information that you judge necessary.
- Add pagination to allow the user to navigate the repositories, 10 by 10.
- Please use Redux or MobX as state management


# Guidelines

- Write clean, readable and well-structured code.
- Version-control with Git and write good commit messages.
- Write concise and well-targeted tests.

# Data

## Input

```
{"0":
  [{"id": 10,
    "title": "House",
    "level": 0,
    "children": [],
    "parent_id": null}],
 "1":
  [{"id": 12,
    "title": "Red Roof",
    "level": 1,
    "children": [],
    "parent_id": 10},
   {"id": 18,
    "title": "Blue Roof",
    "level": 1,
    "children": [],
    "parent_id": 10},
   {"id": 13,
    "title": "Wall",
    "level": 1,
    "children": [],
    "parent_id": 10}],
 "2":
  [{"id": 17,
    "title": "Blue Window",
    "level": 2,
    "children": [],
    "parent_id": 12},
   {"id": 16,
    "title": "Door",
    "level": 2,
    "children": [],
    "parent_id": 13},
   {"id": 15,
    "title": "Red Window",
    "level": 2,
    "children": [],
    "parent_id": 12}]}
```

## Output

```
[{"id": 10,
  "title": "House",
  "level": 0,
  "children":
   [{"id": 12,
     "title": "Red Roof",
     "level": 1,
     "children":
      [{"id": 17,
        "title": "Blue Window",
        "level": 2,
        "children": [],
        "parent_id": 12},
       {"id": 15,
        "title": "Red Window",
        "level": 2,
        "children": [],
        "parent_id": 12}],
     "parent_id": 10},
    {"id": 18,
     "title": "Blue Roof",
     "level": 1,
     "children": [],
     "parent_id": 10},
    {"id": 13,
     "title": "Wall",
     "level": 1,
     "children":
      [{"id": 16,
        "title": "Door",
        "level": 2,
        "children": [],
        "parent_id": 13}],
     "parent_id": 10}],
  "parent_id": null}]
```
