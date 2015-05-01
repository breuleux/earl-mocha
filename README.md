
earl-mocha
==========

Macro wrappers over `mocha` for use with the Earl Grey programming
language.

Usage:

In `test/test.eg`:

    require-macros:
       earl-mocha ->
          describe, it, before, after, assert, expect-error

    describe "testing":
       before:
          @one = 1
          @two = 2
       it "is fun!":
          assert @one + @one == @two
       it "is dangerous!":
          expect-error TypeError:
             null.forbidden-field

Then you can run the command as:

    mocha --compilers eg:earlgrey/register

You will need to `npm install earlgrey --save-dev` for this to work.

If you put `--compilers eg:earlgrey/register` in `test/mocha.opts`,
you can also simply run `mocha`.

