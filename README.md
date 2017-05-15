# NgSQLiteOrm
library that help to buil complete modele for cordova or ionic project with database management.

# Notes
* It is based on the distributing sources files and supports `aot` build
* It works well as dependency form regular [@angular/cli] and [Codova] project or ejected one
* It has demo app, that could be used as documentation or sandbox. Use `ng serve -o true` to run it.
* It exposes only `lib` directory.  


[TL;DR] See [@ns/ng-demo-app] and [live demo].
# Usage
 * create new [@angular/cli] project: `ng new ng-demo-app --style scss`
 * install library: `npm install --save git://git@github.com:nsmolenskii/ng-demo-lib.git`
 * add module import declaration in `app.module.ts`:
 ```typescript
    import { BrowserModule } from '@angular/platform-browser';
    import { NgModule } from '@angular/core';
    import { FormsModule } from '@angular/forms';
    import { HttpModule } from '@angular/http';
    import { MaterialModule } from '@angular/material';
    
    import { AppComponent } from './app.component';
    import { GreeterModule } from 'ng-demo-lib';

    @NgModule({
      declarations: [
        AppComponent
      ],
      imports: [
        BrowserModule,
        FormsModule,
        HttpModule,
        MaterialModule.forRoot(),
        GreeterModule
      ],
      providers: [],
      bootstrap: [AppComponent]
    })
 ```
 * use `demo-greeter` in `app.component.html`: ```<demo-greeter name="Peter Pan"></demo-greeter>```
 * run project: `ng serve -o true`
 * profit

[@angular/cli]: https://github.com/angular/angular-cli
[@ns/ng-demo-app]: https://github.com/nsmolenskii/ng-demo-app
[live demo]: https://nsmolenskii.github.io/ng-demo-app/
[angular/angular-cli#1692]: https://github.com/angular/angular-cli/issues/1692
