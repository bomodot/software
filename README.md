# Stark

stark generates random and strong passwords

the password can include the following characters

```
lowercase      abcdefghijklmnopqrstuvwxyz
uppercase      ABCDEFGHIJKLMNOPQRSTUVWXYZ
digits         0123456789
letters        abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ
alphanumeric   abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789
hexdigits      0123456789abcdefABCDEF
symbols        !"#$%&\'()*+,-./:;<=>?@[]^_`{|}~
```

### Installation

```
pip install stark
```

### Usage

#### API

```
from stark import generate

password = generate(length=30,types={'lowercase':15,'digits':10,'symbols':True})
```

#### CLI

```
$ stark [options]
```

Get help about options

```
$ stark --help

usage: stark [options]

stark generates random and strong passwords

optional arguments:
  -h, --help           show this help message and exit
  -ln, --length        password length
  -a, --any            include any character
  -l, --lowercase      include lowercase
  -u, --uppercase      include uppercase
  -d, --digits         include digits
  -s, --symbols        include symbols
  -x, --hexdigits      include hexadecimal
  -an, --alphanumeric  include alphanumeric
  -lt, --letters       include letters

```

### Examples

default password : 25 character alphanumeric

```
$ stark

Ezvx2gwGVvylnNkueHtoLwg77
```

custom length

```
$ stark -ln 50

0alR2vsoy2FsdqALF7oQhzG0GPicS1qitm69u7Yu6Fhq9mcu2Z
```

30 character password, include 15 lowercase, 7 digits and the rest will be symbols

```
$ stark -ln 30 -l 15 -d 7 -s

7\1z]9%g#4r}kk'zn0da]w~1uy9myb
```

30 character password, include 10 hexdigits an the rest will be uppercase and symbols

```
$ stark -ln 30 -x 10 -u -s

N{92D=NB{8FV"D1B\?OI!)BK6$KB3I
```

### License

this project is ditributed under the MIT LICENSE, check [LICENSE](LICENSE) for more details
