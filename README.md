#REVENV

Virtualenv simplified. 

This is a simple wrapper for virtualenv that follows the approach of the [`inve`](https://gist.github.com/datagrok/2199506) and [`pew`](https://github.com/berdario/pew) utilities to start virtualenvs inside subshells rather than sourcing into the current shell. 

This makes usage easier and reduces a lot of the headache involved with managing virualenvs. Functionality is intentionally quite simple. All you need to use `revenv` is to drop the `revenv` script somewhere on your path, and it will take care of the rest. 

### Features

**Simple and light-weight**. 

`revenv` is just one simple bash script. 

**Visual indicators**

Like `virtualenv`, `revenv` makes sure you can see at a glance which virtualenv you have active by prepending it to the beginning of your prompt. It automatically sets things up correctly for both `bash` and `zsh`.

**Clean approach**

Like `inve` and `pew`, `revenv` starts your virtualenv in a sub-shell rather than corrupting your existing shell session. This means your virtualenv is self-contained. Want to load a virtualenv from inside another virtualenv? Go for it, `revenv` follows standard unix principles and will keep everything straight. As soon as you exit one shell you'll be back at the shell that spawned it. 


### Usage

    revenv [ setup | workon | ls | new | rm ]
      
      
    setup		

        Initial config of revenv. Will set a WORKON_HOME (the directory where
        your virtualenvs will live) if one doesn't exist.

    workon [virtualenv name]

        Activate the specificed virtualenv

    ls

        List all virtualenvs in the $WORKON_HOME directory

    new [virtualenv name]

        Create a new virtualenv with the specified name

    rm [virtualenv name]

        Deletes specified virtualenv
			

