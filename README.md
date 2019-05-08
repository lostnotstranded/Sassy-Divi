# Sassy-Divi
An open source, SCSS version of the Divi theme's parent styleshee!

Divi is the world's most popular WordPress theme, but it's CSS file is fairly bloated and the builder itself relies a lot on CSS overrides. Let's change that!

Using SCSS/SASS, you can now update Divi's styling everywhere. Don't like the default color Divi uses? Instead of overriding it in yet another stylesheet/pile of CSS in the <head>, you can just update it with SASS and have a syntactically correct way styling fo your Divi website, no !important needed!
  
I'm designing this alternative, SASSY stylesheet for Divi to be as simple as possible to use, so even a complete web development beginner with no experience with code will be able to use it. That said, you will need to know how to use a compiler. If you don't have one already installed, us this: https://www.cssportal.com/scss-to-css/. As far as compilers go, if you just want to update like, one variable, that's pretty easy to use. But if you want to use the full power of Sass/SCSS, use your own compiler!

# Warning
I guess I should put some kind of liability waiver here or something so nobody sues me lol.

As of this creation Divi is at version 3.22.7. Don't ask me why I used that version. At the time I created this repository that is/was the current, most up-to-date verison of Divi.

That said, Elegant Themes, the makers of the Divi theme, may or may not change their stylesheet some time down the line for a future version of Divi and may break compatibility with this Sassed up version of the stylesheet. They may introduce new modules down the line, for example, and with those require new CSS code be added to the parent stylesheet, CSS code that the this open source SCSS file will not have. Those modules will not have any styling in that case. I am not responsible if that happens. You use this SCSS file of your own free will and choice.

Nevertheless, this repo is open source, so anybody can update the SCSS file with the latest Divi selectors and styling if they commit the time to doing it. That is the intention behind making it open source, so it will be updated faster.

# How to use it
1. Figure out your compiler of choice. COmpile it.

2. Get a child theme. You should always have a child theme, even if you never write custom PHP/CSS/whatever. Read this on why you should always use a child theme: https://almostinevitable.com/wp-opinion-sort-of-do-you-need-a-child-theme/

3. Load up the customised CSS file. You'll need PHP for that. Start with this:

function scss_enqueue {
  wp_enqueue_style( 'scss-divi', get_stylesheet_directory_uri() . '/filename.css' );
}
add_action( 'wp_enqueue_scripts', 'scss-enqueue' );

That will get you started on the right track. Update "filename.css" with whatever you decided to call your newly compiled Divi stylesheet. If you didn't upload the file directly to your child theme folder, but put it inside a nested folder somewhere, you'll need to correct the file path as well.

# Make cool stuff!
