# Ngx-cnpj-validator

> Ngx-cnpj-validator is an ultra simple cnpj validator for Angular.io.

[![basic-merchandising](https://imgur.com/LNOYczf.png)](https://github.com/leopq)

**Disclaimer**: I use this module for personal projects, which means it is designed to fulfill their specific use cases. The code I develop is crafted with reuse and generalization in mind, still, it may or may not fulfill for your requirements. In case it does not, please feel free to submit a pull request, create a fork or contact me at lpachecoquevedo@gmail.com so we can figure something out together. Thank you for reading this!

## Installing

```sh
$ npm install --save ngx-cnpj-validator
```

## Quickstart

#### Import

Import **ngx-cnpj-validator** module in Angular app.

```typescript
import { NgxCnpjValidator } from 'ngx-cnpj-validator'

(...)

@NgModule({
  (...)
  imports: [
    NgxCnpjValidator.forRoot()
  ]
  (...)
})
```

#### Usage

In your template, you can declare the ngx-cnpj-validator as the following:
```html
<form>
    <!-- Input with the CPF validator -->
    <input type="tel" ngx-cnpj [(ngModel)]="user.cnpj" name="userCnpj" #cnpjInput >
    <!-- Show an error message -->
    <div *ngIf="cnpjInput && cnpjInput.errors && cnpjInput.errors.cnpj">
        The CPF provided is not valid.
    </div>
    <!-- Disable the form in case of validation errors -->
    <button [disabled]="!form.valid">
        Submit!
    </button>
</form>

```

### And that's all there is about it.
* Any doubts? Fell free to open an issue.
* Improvements? Pull requests are always come!
* Suggestions? Of course: Let's [talk](https://twitter.com/leopq)!

##### MIT @ Leonardo Quevedo. 2018.