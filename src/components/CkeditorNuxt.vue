<template>
    <ckeditor
            :editor="editor"
            :value="value"
            :config="config"
            :tagName="tagName"
            :disabled="disabled"
            @input="event => $emit('input', event)"
    />
</template>
<script>

    import FullFreeBuildEditor from '@vndywhat/ckeditor5-build-classic-full-with-base64-upload-and-spoiler'
    import CKEditor from '@ckeditor/ckeditor5-vue2'

    export default {
        components: {
            ckeditor: CKEditor.component
        },
        props: {
            value: {
                type: String,
                required: false
            },
            tagName: {
                type: String,
                required: false,
                default: 'div'
            },
            disabled: {
                type: Boolean,
                required: false,
            },
            uploadUrl: {
                type: String,
                required: false
            },
            config: {
                type: Object,
                required: false,
                default: function () {
                }
            }
        },
        data() {
            return {
                editor: FullFreeBuildEditor,
            }
        },
    };
</script>
