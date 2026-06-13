# Blocks

## Project Structure

```
blocks/
    └── dist/
        └── styles/
            └── blocks.css        # The optimised and minimised stylesheet used for production.
    └── src/
        └── styles/
            └── core/
                └── base.css        # CSS stylesheet containing all the base styles.
                └── reset.css       # CSS reset is taken from this repository: https://github.
            └── layout/
                └── grid.css        # Responsive grid using CSS grid.
            └── main.css            # The main stylesheet that imports all seperate files into a single file.
com/hackdanismo/reset
    ├── .nvmrc                      # Config file to set the Node version when using NVM.
    ├── .gitignore                  # Prevent files being added to version control.
    ├── LICENCE                     # The MIT licence.                                
    ├── README.md                   # README markdown file.
    ├── index.html                  # The HTML document to create the webpage for the project.
```

### CSS Reset
It is worth noting that the `CSS reset` used for this project can be found in the `reset` repository: [https://github.com/hackdanismo/reset](https://github.com/hackdanismo/reset). Any changes to the `reset` code, should be added to that repository before updating the `reset.css` stylesheet here.

## Development

### Clone the Repository
To clone the repository, open the terminal and enter the following commands:

```shell
# HTTPS
$ git clone https://github.com/hackdanismo/blocks.git
# SSH
$ git clone git@github.com:hackdanismo/blocks.git

# Change directory
$ cd blocks
# Install any dependencies listed within the package.json file
$ npm install
```

### Optimise and Minimize the CSS
Use the following build command to minify and optimise the `CSS stylesheets`:

```shell
$ npm run build:css
```

+ This will combine all CSS stylesheets within the `src/styles/main.css` stylesheet into a single file.
+ `bun` will be used to optimise and minify the output file for use in production.
+ The output CSS will be generated within this file: `dist/styles/blocks.css`.

Any new CSS stylesheets should be added to the `src/styles/main.css` stylesheet.

## Licence
The project is created by `Dan Jackson` and released under the [MIT licence](https://github.com/hackdanismo/blocks/blob/main/LICENSE).
