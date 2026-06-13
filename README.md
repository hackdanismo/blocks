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
                └── reset.css       # CSS reset is taken from this repository: https://github.com/hackdanismo/reset
            └── layout/
                └── grid.css        # Responsive grid using CSS grid.
            └── main.css            # The main stylesheet that imports all seperate files into a single file.
    ├── .nvmrc                      # Config file to set the Node version when using NVM.
    ├── .gitignore                  # Prevent files being added to version control.
    ├── LICENCE                     # The MIT licence.                                
    ├── README.md                   # README markdown file.
    ├── index.html                  # The HTML document to create the webpage for the project.
```

### CSS Reset
It is worth noting that the `CSS reset` used for this project can be found in the `reset` repository: [https://github.com/hackdanismo/reset](https://github.com/hackdanismo/reset). Any changes to the `reset` code, should be added to that repository before updating the `reset.css` stylesheet here.

## Using Blocks
Once a webpage or application has been setup, add the `blocks.css` stylesheet to the `<head>` section of the page:

```html
<!DOCTYPE html>
<html lang="en">
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Webpage Title</title>

    <!-- Include the blocks CSS stylsheet -->
    <link rel="stylesheet" href="dist/styles/blocks.css">
</html>
```

### Layout

#### Section and Container

```html
<section class="section">
    <div class="container">
        <!-- Page content here. -->
    </div>
</section>
```

#### Grid

```html
<section class="section">
    <div class="container">
        <div class="row">
            <div class="col">col</div>
        </div>

        <div class="row">
            <div class="col-md-12 col-lg-1">col-md-12 col-lg-1</div>
            <div class="col-md-12 col-lg-1">col-md-12 col-lg-1</div>
            <div class="col-md-12 col-lg-1">col-md-12 col-lg-1</div>
            <div class="col-md-12 col-lg-1">col-md-12 col-lg-1</div>
            <div class="col-md-12 col-lg-1">col-md-12 col-lg-1</div>
            <div class="col-md-12 col-lg-1">col-md-12 col-lg-1</div>
            <div class="col-md-12 col-lg-1">col-md-12 col-lg-1</div>
            <div class="col-md-12 col-lg-1">col-md-12 col-lg-1</div>
            <div class="col-md-12 col-lg-1">col-md-12 col-lg-1</div>
            <div class="col-md-12 col-lg-1">col-md-12 col-lg-1</div>
            <div class="col-md-12 col-lg-1">col-md-12 col-lg-1</div>
            <div class="col-md-12 col-lg-1">col-md-12 col-lg-1</div>
        </div>

        <div class="row">
            <div class="col-md-12 col-lg-4">col-md-12 col-lg-4</div>
            <div class="col-md-12 col-lg-4">col-md-12 col-lg-4</div>
            <div class="col-md-12 col-lg-4">col-md-12 col-lg-4</div>
        </div>

        <div class="row">
            <div class="col-md-12 col-lg-3">col-md-12 col-lg-3</div>
            <div class="col-md-12 col-lg-3">col-md-12 col-lg-3</div>
            <div class="col-md-12 col-lg-3">col-md-12 col-lg-3</div>
            <div class="col-md-12 col-lg-3">col-md-12 col-lg-3</div>
        </div>

        <div class="row">
            <div class="col-md-12 col-lg-6">col-md-12 col-lg-6</div>
            <div class="col-md-12 col-lg-6">col-md-12 col-lg-6</div>
        </div>
        <div class="row">
            <div class="col-md-12 col-lg-3">col-md-12 col-lg-3</div>
            <div class="col-md-12 col-lg-9">col-md-12 col-lg-9</div>
        </div>
    </div>
</section> 
```

To see the `grid` boundaries during development, use the `debug` mode by adding the following `data-debug` attribute to the `<html>` element:

```html
<html lang="en" data-debug="true"> ... </html>
```

### Components

#### Card

```html
<section class="section">
    <div class="container">
        <div class="card-container">
            <div class="card">
                <div class="card__content">
                    <p>This is a card.</p>
                    <p>This is a card.</p>
                    <p>This is a card.</p>
                    <p>This is a card.</p>
                </div>
            </div>
            <div class="card">
                <div class="card__content">
                    This is a second card.
                </div>
            </div>
            <div class="card">
                <div class="card__content">
                    This is a third card.
                </div>
            </div>
        </div>
    </div>
</section>
```

#### Card with Images

```html
<section class="section">
    <div class="container">
        <div class="card-container">
            <a href="#" target="_blank" rel="nopener noreferrer">
                <div class="card">
                    <img class="card__image" src="https://picsum.photos/200" alt="Description of image 1.">
                    <div class="card__content">
                        <div class="flow">
                            <p>This is a card.</p>
                            <p>This is a card.</p>
                            <p>This is a card.</p>
                            <p>This is a card.</p>
                        </div>
                    </div>
                </div>
            </a>
            <div class="card">
                <img class="card__image" src="https://picsum.photos/200" alt="Description of image 1.">
                <div class="card__content">
                    <div class="flow">
                        This is a second card. <a href="#" target="_blank" rel="noopener noreferrer">Link example</a>.
                    </div>
                    <div class="card__cta">
                        <a href="#" role="button" class="button button--pill u-full-width">Read more</a>
                    </div>
                </div>
            </div>
            <div class="card">
                <img class="card__image" src="https://picsum.photos/200" alt="Description of image 1.">
                <div class="card__content">
                    <div class="flow">
                        This is a third card.
                    </div>
                    <div class="card__cta u-flex-right">
                        <a href="#" role="button" class="button button--pill">Read more</a>
                        <a href="#" role="button" class="button button--pill">Read more</a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>
```

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
