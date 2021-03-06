# vue-uploader

[![GitHub last commit](https://img.shields.io/github/last-commit/tityus/vue-uploader.svg?style=flat-square)](https://github.com/tityus/vue-uploader)
[![GitHub issues](https://img.shields.io/github/issues/tityus/vue-uploader.svg?style=flat-square)](https://github.com/tityus/vue-uploader/issues)
![GitHub](https://img.shields.io/github/license/tityus/vue-uploader.svg)

Upload async component for Vue and compatible with Vuetify.


## Install

#### Using NPM

```
npm install @tityus/vue-uploader
```

#### Import

``` vue
import VueUploader from '@tityus/vue-uploader';
```

#### In your component

``` vue
<script>
var app = new Vue({
  el: '#app',
  data: {},
  component: {
    VueUploader
  }
})
</script>
```

#### In your template

``` vue
<vue-uploader></vue-uploader>

```

## Configuration (props)

`accept` : `[String, default : '']` : Specifies what file types the user can pick.

`target` : `[String, default : '']` : Target of your API/Backend

`selected` : `[Boolean, default: false]` : Show selected file

`vuetify` : `[Boolean, default: false]` : Transform to vuetify button.

#### Vuetify props

`dark`, `flat`, `fab`, `large`, `outline` : `[Boolean, default: false]` : See more on Vuetify.

`icon` : `[String, default: '']` : Add icon to button.

## Get response from API

You can get response from your API.


#### App component (Template)

``` vue
<vue-uploader @uploadResponse="getResponse"></vue-uploader>
```

You can get file selected

``` vue
<vue-uploader @uploadFile="getFile"></vue-uploader>
```

#### App component (Script)

``` vue
<script>
  methods: {
    getResponse(value) {
      console.log(value);
    }
  }
</script>
```

## Example template

``` vue
<vue-uploader
  accept="image/*"
  vuetify
  target="/api/upload"
  @uploadResponse="getResponse()" // get data from component
  @uploadFile="getFile()"
  vuetify
  outline
  color="indigo"
  large
  icon="cloud_upload" // Material Icon
>
  Select a file // You can change slot's message
</vue-uploader>

```

## Contribution

For contribute, you can help by submitting an issue or a pull request.

## License

[MIT](http://opensource.org/licenses/MIT)
