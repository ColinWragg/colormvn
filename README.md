Public Development Tools
========================
A lot of people bug me asking what kind of scripts and such I use to make development easier.
Here they are.

colormvn
--------
I created colormvn because I was displeased with other Maven-colorizers out there. I wanted something that uses tput and was extensible.
You can customize the output of colormvn by creating a ~/.colormvn file. It will be sourced by the colormvn script, so you can perform arbitrary processing. Ultimately, the script will look for three variables:
 * Warning
 * Error
 * Info

Here's my personal ~/.colormvn file:
    Warning=$(tput bold)$(tput setaf 11)
    Info=$(tput setaf 33)
    Error=$(tput bold)$(tput setaf 9)
