# AngularHelloWorld

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 15.0.0.

## Option 1: Build & Run app
- `npm install`
- Run `npm run start`
- Navigate to `http://localhost:4200/`.

## Option 2: Build & Run app
- `npm install`
- `npm i -g @angular/cli`
- Run `ng serve`
- Navigate to `http://localhost:4200/`.



## Openrewrite upgrade

Want to upgrade to Angular 17/19 using OpenRewrite

- Already setup moderna account and configured token & sync moderne recipes.

- Follow https://docs.openrewrite.org/recipes/codemods/migrate/angular/applyangularcli

- `mod config recipes jar install org.openrewrite.recipe:rewrite-codemods-ng:0.7.2`

- `mod run . --recipe ApplyAngularCLI --recipe-option "version=17"` OR also tried `mod run . --recipe v19` 

- Error

Recipe run failed with an exception:
org.openrewrite.polyglot.RemoteException: java.lang.RuntimeException: java.io.IOException: Cannot run program "npm" (in directory "C:\Users\shyam\AppData\Local\Temp\rewrite-work15195988347361878869\cycle1_recipe0\repo"): CreateProcess error=2, The system cannot find the file specified
java.lang.RuntimeException: java.io.IOException: Cannot run program "npm" (in directory "C:\Users\shyam\AppData\Local\Temp\rewrite-work15195988347361878869\cycle1_recipe0\repo"): CreateProcess error=2, The system cannot find the file specified
  org.openrewrite.shell.exec.ShellExecutor.exec(ShellExecutor.java:69)
  org.openrewrite.shell.exec.ShellExecutor.exec(ShellExecutor.java:40)
  org.openrewrite.codemods.migrate.angular.NodeBasedRecipe.runNode(NodeBasedRecipe.java:141)
  org.openrewrite.codemods.migrate.angular.NodeBasedRecipe.generate(NodeBasedRecipe.java:83)
  org.openrewrite.codemods.migrate.angular.NodeBasedRecipe.generate(NodeBasedRecipe.java:29)
  org.openrewrite.ScanningRecipe.generate(ScanningRecipe.java:72)
  org.openrewrite.scheduling.RecipeRunCycle.lambda$generateSources$5(RecipeRunCycle.java:134)
  org.openrewrite.scheduling.RecipeStack.reduce(RecipeStack.java:57)





