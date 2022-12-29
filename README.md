# Mon Cash Package For Laravel - MRVIVALDIO

This is the PHP SDK that allows php's developers to interract with the MonCash payment facility on their website.
This is an advanced version of the moncash PHP SDK.
These codes have been modified at the company M7ROV Consolidate by the developer R. Vivaldi O MAURICE in order to facilitate web development with laravel, php and moncash at the same time.

## Structure

We habe used the following industry bes practices for structuring for this SDK.

```xpath
src/
    |
     M7C/
        |Adapter/
        |Contracts/
        |Exception/
        |Http/
        |Relation/
        |View/
        
     Moncash/
            
    helpers.php
tests/
```

## Install

Via Composer

``` bash
# composer require mrvivaldio/moncash
```

## Usage

### This package (library) is not complete for Laravel, however it is easy to use with PHP.
Only one instance of "setup" is necessary on the view of your choice.
1) You are free to choose to pass data as parameters



```injectablephp
use Mrvivaldio\M7C\View\Setup;
$setup = new Setup($your_secret, $your_client, $the_card_reference, $total_to_charge);
```

2) You can instantiate and then use the setters
```injectablephp
$setup = new Setup();
$setup->setSecret($your_secret);
$setup->setClient($your_client);
$setup->setOrder($the_card_reference);
$setup->setAmount($total_to_charge);
```

To list the transactions, this same variable can be used (An html table tag will do the trick)
```injectablephp
$setup->transaction()->reference;
$setup->transaction()->id;
$setup->transaction()->balance;
$setup->transaction()->message;
$setup->transaction()->pay;
$setup->transaction()->date;
```

As it is not yet complete, I will make sure that it is portable, that is to say, usable on both pure PHP and Laravel.

Don't forget to put a little star to encourage me.
If you want help, I am available at ``` +509 44 22 9600```.


### Ce package (librairie) n'est pas terminé pour Laravel, par contre il est simple d'usage avec PHP.

Une seule instance de "setup" est nécessaire sur la vue de votre choix.
1) Vous êtes libre de choisir de passer des données en paramètres

```injectablephp
use Mrvivaldio\M7C\View\Setup;
$setup = new Setup($your_secret, $your_client, $the_card_reference, $total_to_charge);
```


2) Vous pouvez instancier, puis utiliser les setters

```injectablephp
$setup = new Setup();
$setup->setSecret($your_secret);
$setup->setClient($your_client);
$setup->setOrder($the_card_reference);
$setup->setAmount($total_to_charge);
```


Pour lister les transactions, cette même variable peut-être utiliser (Une balise table html fera bien l'affaire)

```injectablephp
$setup->transaction()->reference;
$setup->transaction()->id;
$setup->transaction()->solde;
$setup->transaction()->message;
$setup->transaction()->payer;
$setup->transaction()->date;
```

Comme ce n'est pas encore complet, je ferai en sorte qu'elle soit portable, c'est-a-dire, utilisable à la fois sur PHP pur et Laravel.

N'oublie pas de mettre une petite étoile pour m'encourager.
Si vous voulez de l'aide, je suis disponible au ```+509 44 22 9600```.

## Testing

``` bash
$ phpunit --bootstrap vendor/autoload.php tests/.
```


## Security

If you discover any security related issues, please email rulxphilome.alexis@gmail.com instead of using the issue tracker.
This is a direct reference to Moncash.
## Credits

- M7ROV Consolidate https://instagram.com/m7rovconsolidate
- R. Vivaldi O MAURICE https://mrvivaldio.com

## License
- M7ROV Consolidate
- To be filled by MonCash
