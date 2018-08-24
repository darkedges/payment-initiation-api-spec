# payment-initiation-api-spec

# Version
This is version v1.1.1  
A Patch Release

## Change Control
Change since v1.1.0 
* Remove `tpp_client_credential` scope and replace with `payments` scope


# Usage
You need to define a `VERSION` variable, values can be one of `v1.0 | v1.1`
```export VERSION=v1.1```

```npm run start```  builds the project and runs a local webserver on http://localhost:8080/ serving the swagger spec using the spectacles-docs format

# Scripts
```npm run test``` runs the tests , validate swagger spec against the swagger schema (not the editor!!)

```npm run flatten-schemas``` flattens the schemas in the schema folder<br>
```npm run compile-swagger``` dereference the swagger spec split from  several yaml files to one fully dereferenced yaml file , dereferencing the schemas compiled using npm run flatten-schemas

# Versions
The buid scripts depend on a version being set in an environment variable 
e.g. export `VERSION=v1.0`  
The Master list of allowable versions is stored in the /build/versions.js file 
and must be maintained there as new versions are created.


****WIP Documentation****
To convert SwaggerSpec to MARKDOWN
You need to have
1) swagger2markup-cli-1.3.1.jar  -> http://swagger2markup.github.io/swagger2markup/1.3.1/#_command_line_interface
this JAR file needs to be saved in the root directory of the project for it to work 
2) asciidoctor
   gem install asciidoctor
3) ruby 2.2
4) asciidoctor-pdf
(ruby v2.2)
- rvm install 2.2
- rvm use 2.2
- gem install --pre asciidoctor-pdf
- gem uninstall prawn
- gem install prawn -v 2.1.0
