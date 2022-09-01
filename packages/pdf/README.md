# NativeScript PDF

> *Remark* [This repository](https://github.com/NativeScript/plugins/blob/main/packages/pdf) is the replacement for [madmas/nativescript-pdf-view](https://github.com/madmas/nativescript-pdf-view) which was a fork of [the original by Merott](https://github.com/Merott/nativescript-pdf-view) and will be used with his consent to provide further maintenance of this NativeScript plugin.

It serves minimal PDF view implementation that does only one thing, and that is to display PDF files in the simplest way possible. It conveniently uses the iOS `WKWebView`, and for Android it uses [`AndroidPdfViewer`](https://github.com/barteksc/AndroidPdfViewer).

This plugin does the bare minimum required to render the PDF, no configuration options, and no error handling have been built yet. All Pull Requests to enhance its functionality are welcome!

The aim is to keep the features consistent across iOS and Android.

## Installation

```
tns plugin add @nativescript/pdf
```

## Usage

### Vanilla NativeScript

```xml
<Page
  xmlns="http://schemas.nativescript.org/tns.xsd"
  xmlns:pdf="@nativescript/pdf"
  loaded="pageLoaded">
  <pdf:PDFView src="{{ pdfUrl }}" load="{{ onLoad }}" />
</Page>
```

### Angular NativeScript

```ts
import { NativeScriptPdfModule } from '@nativescript/pdf/angular'

...

@NgModule({
	imports: [
    NativeScriptCommonModule, 
    ...
    NativeScriptPdfModule],
...

```

```html
<PDFView [src]="src" (load)="onLoad()"></PDFView>
```

## Demo

Check out the [demo](./demo) folder for a demo application using this plugin. You can run the demo by executing `npm run demo.ios` and `npm run demo.android` from the root directory of the project.


## Samples

There are sample applications avalable:

* *Plain TypeScript*: see [pdf.ts](https://github.com/NativeScript/plugins/tree/main/apps/demo/src/plugin-demos/pdf.ts) and [pdf.xml](https://github.com/NativeScript/plugins/tree/main/apps/demo/src/plugin-demos/pdf.xml) files in this repository
* *NativeScript+Angular*: [nativescript-pdf-view-angular-sample](https://github.com/madmas/nativescript-pdf-view-angular-sample) repository
* *NativeScript+VueJs*:  [nativescript-pdf-view-vue-sample](https://github.com/madmas/nativescript-pdf-view-vue-sample) repository