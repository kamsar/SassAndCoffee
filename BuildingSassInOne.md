# How to build Sass-In-One

1. Check out Sass.
2. Copy the ext/build\_sass\_in\_one.rb script to the sass/lib directory.
3. ruby build\_sass\_in\_one.rb > sass\_in\_one.rb 2>log.txt - this will
   probably throw a few errors.
4. Keep trying to run sass\_in\_one.rb and fixing up the runtime errors 
   (Sass tries to build its version info from files in the Gem - replace
    it with hardcoded strings)
5. Find the line with "scope('VERSION')" and replace that line with the hardcoded version of sass. Something like: "numbers = "3.2.9".strip.split('.')."
6. Find the line with "scope('VERSION_NAME')" and replace that line with the hardcoded version name. Something like: "name = "Media Mark"."