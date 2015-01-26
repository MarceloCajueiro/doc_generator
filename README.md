# Doc generator

This is a simple project in Go that I made while studying the language.

## CPF and CNPJ generator

You can use the bin to generate those documents with:

```
$ doc_generator cpf
$ doc_generator cnpj
```

## Generate the binary by yourself

If you have Golang installed you can clone this project in your machine and
build the bin:

```
$ cd $GOPATH/src
$ git clone https://github.com/MarceloCajueiro/doc_generator.git

$ cd doc_generator

$ go build
```

Now you have the bin `doc_generator`.

You can also install the bin with `$ go install`. To this work you have add the
go bin dir to the PATH variable:

```
export PATH=$PATH:$GOPATH/libexec/bin
export PATH=$PATH:$GOPATH/bin
```

Now every Go software installed with `$ go install` will work properly in any
location of the shell.

## Clipboard

You can copy the output to the clipboard:

### Mac

`$ doc_generator cpf | pbcopy`

### [Some Linux distros](http://stackoverflow.com/questions/5130968/how-can-i-copy-the-output-of-a-command-directly-into-my-clipboard)

```
$ sudo apt-get install xclip
$ doc_generator cpf | xclip
```

## Aliases

You can also add aliases to bash (or other Unix shell):

```
alias cpf="doc_generator cpf"
alias cnpj="doc_generator cnpj | pbcopy"
```

## ...

I don't know if anyone will use this, but it is being useful to me and I had fun
in the development. :D

## Credits

I grabbed the algorithms at: http://www.geradorcpf.com/
