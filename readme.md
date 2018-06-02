# Fable Elmish with React renderer Template 

## Build and run dev server

- [Paket-Bootstrap](https://gist.github.com/maestrow/94d99017380adbcadff29f048f423729#file-paket-bootstrap-md)
- `npm install` or `yarn install`
- `cd src`
- `dotnet restore`
- `dotnet fable {npm|yarn}-{build|start}`. Or `dotnet fable start` and then `npm {build|start}`


## Create Fable Elmish with React renderer Template from scratch

- `git clone https://github.com/funcysharp/fable-tpl`

- Add Elmish: 
    
    paket add Fable.Elmish --project .\src\MyProject.fsproj
    
- Add Elmish React renderer:
    
    paket add Fable.Elmish.React --project .\src\MyProject.fsproj
    npm i -S react react-dom 
    
- Other stuff

    npm i -D babel-plugin-transform-runtime
    npm i -D copy-webpack-plugin
    ...
    
- Add [src/index.html](https://github.com/fable-elmish/sample-react-counter/blob/master/src/index.html) and `webpack.config.js`


## See also

- [Create Fable Application manually from scratch](https://gist.github.com/maestrow/70ed3fcee7127cac9b860923ea5e76a2)


## Packages update

Be carefull when update webpack related packages. It always unpredictable.

- https://github.com/webpack/webpack-cli/issues/477

Always check `npm run build` and `npm run start` (after `dotnet fable start`) commands before commit package updates.