# NpmPackage

This project was generated using [Angular CLI](https://github.com/angular/angular-cli) version 20.1.6.

## Tools
* Reactive form validator
* Numbers only validator (Use in input where type is text or string)

## Install the package

Install package using npm

```bash
npm i ng-core-helpers
```

* Reactive form validator
## Create Ng Reactive Form

```bash
  public employeeForm = new FormGroup<IEmployeeForm>({
    id: new FormControl(0),
    firstName: new FormControl('', [Validators.required, Validators.minLength(3), Validators.maxLength(15)]),
    lastName: new FormControl('', [Validators.required, Validators.minLength(3), Validators.maxLength(15)]),
    email: new FormControl('', [Validators.required, patternWithMessage(/^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/, 'Please enter a valid email address (e.g. example@domain.com).')]),
    contact: new FormControl('', [Validators.required, patternWithMessage(/^[6-9]\d{9}$/, 'Please enter a valid contact number.')]),
    userType: new FormControl('', [Validators.required]),
    address: new FormControl('', [Validators.required,  Validators.maxLength(70)]),
    username: new FormControl(null, [Validators.minLength(3), Validators.maxLength(30)]),
    password: new FormControl(null, [Validators.minLength(8), Validators.maxLength(8)]),
    isLogin: new FormControl(false),
  });
```

## Use in HTML

```bash
<input
  class="w-full border border-slate-300 rounded-[5px] px-3 py-2 pl-10 pr-10 text-sm text-gray-800 placeholder-slate-400
         focus:ring-[#82181A] focus:outline-none focus:border-[#82181A] transition duration-200 text-base"
  type="text"
  placeholder="Enter first name"
  formControlName="firstName"
  minlength="3"
  maxlength="15"
  libValidateNgReactiveForm
/>

```

* Numbers only validator (Use in input where type is text or string)
## Use in HTML
```bash
<input
  class="w-full"
  type="text"
  formControlName="contact"
  minlength="3"
  maxlength="15"
  libNumberOnlyDirective
/>

```
