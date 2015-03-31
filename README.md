
earl-mocha
==========

Macro wrappers over `mocha` for use with the Earl Grey programming
language.

Usage:

    require-macros:
       earl-mocha ->
          describe, it, before, after, assert, expect-error

    describe "testing":
       before:
          @one = 1
          @two = 2
       it "is fun!":
          assert @one + @one == @two
       it "is dangerous!"
          expect-error [Error?]:
             null.forbidden-field

