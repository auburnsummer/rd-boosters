This repository contains the data for the "booster pack" functionality of the [rdlevels](https://auburnsummer.github.io/rdlevels) website.

## Expected Formats

It uses the YAML format. Here's a primer on the expected format of the `boosters.yaml` file, which is the data source for the booster names and descriptions:

 * The root level element of `boosters.yaml` is an array;
 * Each element in the array is an object with these keys:
    * `title`: The title of the starter pack
    * `description`: The description of the starter pack
    * `file`: The name of the .yaml file that contains the levels for the starter pack, **without the .yaml extension**.

Please look at the existing `boosters.yaml` file as an example.

The other .yaml files expect this format:

 * The root level element is an array;
 * Each element in the array is an object with these keys:
   * `take`: The number of levels to randomly select in this group of levels
     * Do not add a trailing comma: `- take: 2,` and `- take: 2` are different things
     * A `take` value larger than the actual number of levels just means "always take all the levels in this group".
   * `levels`: A array of urls to levels.
     * I'm using JSON-style arrays here to avoid sneaky indentation errors with nested YAML arrays
   
Please look at the existing files for examples.

Make sure to run your edits through a validator (such as http://www.yamllint.com/), before pushing a change.
