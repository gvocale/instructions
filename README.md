# Angular
## Instructions

### Set globally to SCSS

    ng set defaults.styleExt=scss --global

### Create project

    ng new my-dream-app
    cd my-dream-app


### Expand webpack config file

    ng eject


### Install Pug

    npm i -D pug pug-ng-html-loader

Edit webpack.config.js in root of of the project and add:

    module.exports = {
      module: {
        rules: [
          {
            test: /\.(pug|jade)$/,
            use: ['pug-ng-html-loader']
          }
        ]
      }
    }

Then your components can use pug

    @Component({
      selector: 'app-root',
      templateUrl: './app.component.pug',
      styleUrls: ['./app.component.styl']
    })



### SCSS
Move `styles.scss` to `src/scss/styles.scss`

Edit `.angular-cli.json`

    "styles": [
      "scss/styles.scss"
    ],
      
Edit `webpack.config.js`

    "styles": [
      "./src/scss/styles.scss"
    ]
    
Create subfolder structure in `src/scss`

    scss/base
    scss/mixins
    scss/tools
    scss/variables
    
Import them in `src/scss/styles.scss`

    @import 'base/base.scss';
    @import 'mixins/mixins.scss';
    @import 'tools/tools.scss';
    @import 'variables/variables.scss';



### Run app
`npm start`


### Generate components
`ng g component navbar`
