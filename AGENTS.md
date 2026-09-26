# Working on the Glass Mirror scaffold

`application.rb` contains Sinatra routes; `helpers/`, `models/`, `views/`, and
`db/migrate/` contain integration helpers, persistence, templates, and migrations.
The tracked helper is `helpers/yoursharehelper.rb`; the README's
`yourservicehelper.rb` reference is not the actual filename.

Use compatible Ruby dependencies from `Gemfile.lock` with `bundle install` and
a disposable PostgreSQL database. README starts the app with
`bundle exec unicorn`. This connects OAuth, Google Mirror, and S3 integrations;
do not launch against real accounts for a routine check or print configuration.

No automated tests or lint/typecheck task are declared. Use
`ruby -c <changed-ruby-file>` for syntax and a targeted disposable integration
check for route or database behavior. Rake loads `application.rb`, so even task
discovery can initialize application dependencies. Do not treat migrations or
outbound sharing as harmless verification. Do not read or commit runtime logs.

## Completing changes

Follow existing patterns and carry authorized work through the relevant checks,
repairing failures caused by the change. Choose routine implementation details
directly; ask only when missing information materially changes scope or outcome.
For documentation-only edits, check the diff, referenced paths, and command
accuracy rather than starting application runtimes. If a prerequisite blocks a
check, report the exact blocker and continue independent authorized work. Close
with changed paths, checks actually run and results, and remaining unverified
behavior; distinguish commands inspected from commands executed.
