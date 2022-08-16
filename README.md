# Goal
Monorepo with one main package that contains the app and a second package that
contains all the translations.

# Expected behaviour
The generated translations (`intl` package) are exported by the `translation` 
package. The `main_app` imports the translation package and by including the
`translation.dart` file it could access to all the translations. This is the
same behaviour that we got with non-generated files (see `foo.dart`).

# Actual behaviour
The generated files can't be exported. While the non-generated files can. The
IDE does not even report a warning.