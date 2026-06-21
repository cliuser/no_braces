# no_braces

Display all braces as significant whitespace, for code browsing in neovim. less noise.

Inspired by joeytwiddle/signicant-whitespace, found by Google search.

I didn't realize how ___annoying___ braces are until I compiled and learned python (1.3b2!). Now they drive me crazy when I work in all the braced or begin/end languages. (Yes, I'm thinking of you, Ada.) I can't change the filetype since it would muck with everything else. So ... either put a converted version in /tmp and read that as text (clang-format/astyle $opts $file | unexpand -t 4 > /tmp/$file.txt; convert, and reload) which loses all the highlighting and won't parse (useless). So use virtual text ala markview and rendermarkown. It might be as simple as _hiding_ braces and semicolons.

nvim is forced to "noet ts=4".
clang is installed on OS, so "set equalsprog=clang-format"
File needs to be beautified first. Let treesitter/clang do it. TODO: pick style.
Upgrade any antique K&R C code to ANSI and autosave: TODO. Yes, it's still out there.
TODO: Disable rainbow-delimiters?
