# Angular 4
## Instructions

### Set globally to SCSS
`ng set defaults.styleExt=scss --global`

### Create project
`ng new my-dream-app
cd my-dream-app`


### Expand webpack config file
`ng eject`


### Install Pug
`npm i -D pug pug-html-loader`

Edit webpack.config.js in root of of the project and add:

`module.exports = {
  module: {
    rules: [
      {
        test: /\.(pug|jade)$/,
        use: ['pug-ng-html-loader']
      }
    ]
  }
}`

Then your components can use pug

`@Component({
  selector: 'app-root',
  templateUrl: './app.component.pug',
  styleUrls: ['./app.component.styl']
})`



### SCSS
Move `style.scss` to `src/scss/style.scss`

Edit `.angular-cli.jason`
`      "styles": [
        "scss/styles.scss"
      ],`


### Run app
`npm start`
