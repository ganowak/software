# SUSY Software documentation

The purpose here is to document some important SUSY Generators that is useful for the group. 

## IsaJet

### Installation 

You should download the latest version [here](https://www.nhn.ou.edu/~isajet/). The [tarball](http://www.nhn.ou.edu/~isajet/isajet.tar) file contains all the package contents. 

You can instead download the tarball via `wget` as 

```
wget http://www.nhn.ou.edu/~isajet/isajet.tar
```

Then you will need to untar

```
tar -xvf isajet.tar & rm isajet.tar
```

The instllation is pretty simple process, you would need to make sure you have `gfortran` compiler instllaed on your system because this package is written in Fortran. If you don't have the compiler then jump to next section. 

After that you just need to compile using 

```
make
```

Then you are ready to use IsaJet

### Usage 

There are two ways of using IsaJet. There is is interactive way which is you interacting via terminal script and choose models/ modify parameters. The other is a little bit involved and you need to know a little bit of fortran and it is explained [here](http://www.nhn.ou.edu/~isajet/isajet788.pdf)

The interactive method is easy to use. You need to run 

```
./isasugra.x
```
* Make sure that you are in the main directory of IsaJet. 

You will be prompted to enter output file name in a single quote. For example you can write

`isajet_test_file`

This file is where the log will be saved 

after that you will prompted to enter the output for SLHA file. For example you can write 

`isajet_test_file.slha`

Then again it will ask you for Herwig interface filename (don't know about) but if you don't need it (most probably) just write `/` and then click `<enter>`

You will be prompted now to choose the current implemented models inside isajet and when you choose a number it will prompted you to enter this model parameters. For example let us take model # 2 which is  `mGMSB` or minimal gauge mediated supersymmetry breaking model. When we click 2 and `<enter>` we will be given a message like `ENTER Lambda, M_mes, N_5, tan(beta), sgn(mu), M_t, C_gv:`
We need to be careful and enter the values in order. The explanation for the parameters are:

|           |                                                                                                                                             |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| Lambda    | SUSY breaking scale                                                                                                                         |
| M_mes     | the mass scale of the SUSY loop messengers                                                                                                  |
| N_5       | The number of messenger super multiplets                                                                                                    |
| tan(beta) | The ratio of the vacuum expectation values of the two neutral Higgs fields                                                                  |
| sgn(mu)   | The sign of the Higgs mass parameter                                                                                                        |
| M_t       | Mass of the top quark (isajet probably the only susy package that require manual input of this value instead of using pre-defined SM value) |
| C_gv      | Parameter affects gravitino mass                                                                                                            |

Choose the values and put `,` between each value and the other. when you click `<enter>` it will take a moment to do the calculations 


After it is done you will find both the log file `isajet_test_file` and `isajet_test_file.slha` in the same directory. 