# ckeditor5-custom-build-reach

This is a custom build of CKEditor 5 based off of the [Classic Editor](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/overview.html#classic-editor). It is meant to use paired with the [official React component](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/integration/frameworks/react.html).

The [original documentation](https://ckeditor.com/docs/ckeditor5/latest/examples/builds/classic-editor.html) stands true for the most part. For the part that it differs, it will be highlighted in this README.

--

## Quick start

Add it to your project:

```bash
npm install @ckeditor/ckeditor5-react ckeditor5-custom-build-reach
```

And use it as a component like so:

```code
import CKEditor from '@ckeditor/ckeditor5-react';
import CKEditorReach from 'ckeditor5-custom-build-reach';

<CKEditor
  editor={ CKEditorReach }
  data="<p>Hello from CKEditor 5!</p>"
  onInit={ editor => {
    // You can store the "editor" and use when it is needed.
    console.log( 'Editor is ready to use!', editor );
  } }
  onChange={ ( event, editor ) => {
    const data = editor.getData();
    console.log( { event, editor, data } );
  } }
  onBlur={ ( event, editor ) => {
    console.log( 'Blur.', editor );
  } }
  onFocus={ ( event, editor ) => {
    console.log( 'Focus.', editor );
  } }
/>
```

## License (imported from the original repo)

Licensed under the terms of [GNU General Public License Version 2 or later](http://www.gnu.org/licenses/gpl.html). For full details about the license, please check the `LICENSE.md` file or [https://ckeditor.com/legal/ckeditor-oss-license](https://ckeditor.com/legal/ckeditor-oss-license).
