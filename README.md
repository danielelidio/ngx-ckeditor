# ngx-ckeditor
[ ![Travis CI Status](https://travis-ci.org/HstarComponents/ngx-ckeditor.svg?branch=master)](https://travis-ci.org/HstarComponents/ngx-ckeditor)

The CKEditor component for angular(2.x and 4.x)

# Usage

## Installation

- Import CKEditor js file

```html
<script src="//cdn.ckeditor.com/4.7.1/full/ckeditor.js"></script>
```

- Install `ngx-ckeditor`

```bash
npm i -S ngx-ckeditor
```

## Sample

Import `CKEditorModule` module in your main module: 

```
// app.module.ts

import { CKEditorModule } from 'ngx-ckeditor';

@NgModule({
  imports: [
    // ...
    CKEditorModule
  ],
  // ...
})
export class AppModule {

}
```

Then use it in your component:

```html
// app.component.html

<ck-editor name="editor1" [(ngModel)]="editorValue" skin="moono-lisa" lang="en" [fullPage]="true"></ck-editor>
```

```js
// app.component.ts

@Component({
  selector: 'app',
  templateUrl: 'app.component.html'
})

export class AppComponent implements OnInit {

  public editorValue: string = '';

  ngOnInit() { }
}
```

## `CKEditorComponent` Options

| Type | Name | DataType | Default Value | Description |
| --- | --- | --- | --- | --- |
| Input | readonly | boolean | false | Enabled / disable readonly on editor |
| Input | skin | string | 'moono-lisa' | Set the editor skin |
| Input | language | string | 'en' | Set the editor language |
| Input | fullPage | boolean | false | Enalbed /disable fullPage mode on editor |
| Input | config | object | {} | CKEditor's config object, [see more](http://docs.ckeditor.com/) |
| Two-way | ngModel | string | | Two-way binding value |

# How to develop?

```bash
git clone https://github.com/HstarComponents/ngx-ckeditor.git

# install deps
npm i 

# run dev
npm run dev

# build demo
npm run build

# build aot demo
npm run build:aot
```

# Issues

[Create an issue](https://github.com/HstarComponents/ngx-ckeditor/issues/new)

# License

[MIT License](https://github.com/HstarComponents/ngx-ckeditor/blob/master/LICENSE)
