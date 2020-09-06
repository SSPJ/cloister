## The Specs

Basics

1. cloister is a single script or binary (provided the language allows that)
1. cloister has no external dependency
1. cloister accepts 0 or 1 parameters

    When called with 0 parameters, output the user's current exercise and a list of all exercises which are both unlocked and not yet complete.

    When called with 1 parameter, mark that exercise as in progress.

Implementation

Each Exercism track contains a `config.json`.

```
{
  ...
  "exercises": [
    {
      "slug": "hello-world",
      "uuid": "4fe19484-4414-471b-a106-73c776c61388",
      "core": true,
      "auto_approve": true,
      "unlocked_by": null,
      "difficulty": 1,
      "topics": [
        "strings"
      ]
    },
    ...
  ],
  ...
}
```

Cloister interacts with this file by adding keys to the exercises.

1. `completed` - boolean, optional

    If this key is missing or false, the user has not completed that exercise.

1. `current` - boolean, optional

    If this key is present and true, the user is working on that exercise.

Additionally, cloister makes use of two existing properties.

1. `slug` - string

    The human readable name of the exercise. Not globally unique, but unique within a language track.

1. `unlocked_by` - string or null

    If not null, contains the slug of the exercise which must be marked completed before the user can progress to that exercise.

    Cloister does not enforce this. Cloister's use of this variable is limited to generating the list of exercises to suggest.

### Compiled languages

Do not submit a binary. Put the cloister source code in the appropriate folder structure. Add compilation instructions to the main [README](README.md).

## Language specific notes

In lieu of a README for each version of cloister, please put any language dependent notes in here. If it effects installation or usage, put it in the main [README](README.md), also.

### Python

None.

### Ruby

None.
