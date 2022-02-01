# ckeditor-nuxt

CKEditor 5 editor for nuxt apps. The component includes all free available plugins (plus Spoiler plugin) (except CKFinder, instead simple upload adapter used)
Simpliest fork of @lightdelusion (Thanks, man!)

## Requirements

```
yarn add nuxt # OR npm i nuxt
```

## Component integration

```
yarn add @vndywhat/ckeditor-nuxt # OR npm install --save @vndywhat/ckeditor-nuxt
```

## List of included plugins

- Alignment,
- Base64UploadAdapter,
- Autoformat,
- Autolink,
- Autosave,
- BlockQuote,
- Bold,
- Code,
- CodeBlock,
- Essentials,
- FontBackgroundColor,
- FontColor,
- FontFamily,
- FontSize,
- Heading,
- Highlight,
- HorizontalLine,
- Image,
- ImageCaption,
- ImageInsert,
- ImageResize,
- ImageStyle,
- ImageToolbar,
- ImageUpload,
- Indent,
- IndentBlock,
- Italic,
- Link,
- List,
- ListStyle,
- Markdown,
- MathType,
- MediaEmbed,
- PageBreak,
- Paragraph,
- PasteFromOffice,
- RemoveFormat,
- SimpleUploadAdapter,
- SpecialCharacters,
- SpecialCharactersArrows,
- SpecialCharactersCurrency,
- SpecialCharactersEssentials,
- SpecialCharactersLatin,
- SpecialCharactersMathematical,
- SpecialCharactersText,
- Spoiler,
- Strikethrough,
- Subscript,
- Superscript,
- Table,
- TableCellProperties,
- TableProperties,
- TableToolbar,
- TextTransformation,
- Title,
- TodoList,
- Underline,
- WordCount,

## Usage

```
<template>
  <client-only placeholder="loading...">
    <ckeditor-nuxt v-model="contentHolder" :config="editorConfig"  />
  </client-only>
</template>

<script>
export default {
  components: {
    'ckeditor-nuxt': () => import('@vndywhat/ckeditor-nuxt')
  },
  data() {
    return {
      editorConfig: {
        simpleUpload: {
          uploadUrl: 'path_to_image_controller',
          headers: {
            'Authorization': 'optional_token'
          }
        }
      },
      contentHolder: ""
    }
  }
}
</script>


```
