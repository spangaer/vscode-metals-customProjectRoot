Don't really need to do anything.

Just start the DevContainer and allow for all installation to be complete.
(either locally or in codespaces, both should error the same).
`sbt bloopInstall` is run as part of the container start.

Then just go to the metals tab, which will attempt to start metals.
Observe that it starts everything (bloop, looking for format) in the
workspace root.

Given that at that point it's broken, it will also use presentation compiler
v3.3.4 instead of 2.12.x. for all scala files.

If it doesn't break the first time arround, just open the `Run Docter`.
That tends to be sufficient to push it off the cliff.
