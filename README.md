# ld-gif
Gif plugin for [last-draft](http://lastdraft.vace.nz) using [Giphy](https://github.com/Giphy/GiphyAPI)

[![npm version](https://badge.fury.io/js/ld-gif.svg)](https://badge.fury.io/js/ld-gif)

# Install
```jsx
npm install ld-gif --save
```

# Use
```jsx
import {Editor} from 'last-draft'
import gif from 'ld-gif'
let plugins = [gif]

export default class ExampleEditor extends Component {
  constructor(props) {
    super(props)
    const INITIAL_STATE = editorStateFromHtml('<div></div>')
    this.state = { value: INITIAL_STATE }
  }

  onChange(editorState) {
    this.setState({ value: editorState })
  }

  render() {
    return (
      <Editor
        inline={['bold', 'italic', 'code', 'dropcap']}
        blocks={['h2', 'quote']}
        plugins={plugins}
        editorState={this.state.value}
        onChange={::this.onChange} />
    )
  }
}
```

## Styles

Last Draft plugins use styled-components 💅 for the base styling.

## Custom Styles with CSS

You can also add custom css to override the base styling with the following class names specified below:

```css
.ld-gif-modal-wrapper {}
.ld-gif-block-wrapper {}
.ld-gif-block {}
.ld-gif-block-image {}
.ld-gif-block-action {}
.ld-button-gif-close {}
.ld-gif-button {}
.ld-button-gif-picker-close {}
.ld-button-gif-picker-close-wrapper {}

.ld-button-gif-picker-close-button-wrapper {}
.ld-gif-picker-input {}
.ld-gif-picker-wrapper-outer {}
.ld-gif-picker-wrapper {}
.ld-gif-picker-item {}
```
