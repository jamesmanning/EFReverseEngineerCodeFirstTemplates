EFReverseEngineerCodeFirstTemplates
===================================

A set of T4 template files you can use with the Entity Framework Power Tools for generating code-first classes from an existing database.  For more details, see the original blog post from Rowan Miller at http://romiller.com/2012/05/09/customizing-reverse-engineer-code-first-in-the-ef-power-tools/

Steps needed to use these files:

- install Entity Framework Power Tools
  - inside Visual Studio, you can go to the Extension Manager via Tools -> Extensions and Updates and search for "Entity Framework Power Tools" to find and install it.
- Right-click on the project you want to host the resulting classes and select Entity Framework -> Customize Reverse Engineer Tempaltes
  - this will create 3 template files (Context.tt, Entity.tt, Mapping.tt) under a CodeTemplates/ReverseEngineerCodeFirst directory inside your project
- modify the files
  - the simplest option is likely to download the 'raw' files from this repo over top of the files that were created
- Right-click on the project you want to host the resulting classes and select Entity Framework -> Reverse Engineer Code First
  - this will generate the Code First classes for your model.


Known issues
===================================
- Needs to add [ForeignKey] attribute for cases where the convention doesn't correctly work out the FK column
