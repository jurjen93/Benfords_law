# Benford's law analysis

Benford's law is a digit-law, which states that the distribution of seperate digits in numbers follow a specific frequency.
This specific frequency is seen in many numerical datasets, as discovered by Simon Newcomb and Frank Benford.
You can find on [wikipedia] more information about this mysterious law.

Benford's law might be helpful to detect [fraud], do [science], or just investigate the [quality of data].

#### Installation
By ```pip install benfordslaw-analysis``` you will install the package.

#### Usage
Now you can do ```from benfordslaw_analysis import analysis``` to obtain the analysis script.
Here there is the class ```BenfordsLaw``` which you can get with ```analysis.BenfordsLaw```.
Now you can analyse your data by making plots.

For example, make a plot with Benford's law versus random data with:
```
from benfordslaw_analysis.analysis import BenfordsLaw
from random import uniform
random_data = [uniform(-10, 10) for i in range(0,1000)]
bl = BenfordsLaw(random_data)
bl.plot_first_digit()
```
Note that we use the Euclidean distance between the digit frequency from Benford's law and your own data as a measure
and that we use Poisson error bars.

This package is still under development. More updates and documentation will come...

[wikipedia]: https://en.wikipedia.org/wiki/Benford%27s_law
[fraud]: https://www.journalofaccountancy.com/issues/2017/apr/excel-and-benfords-law-to-detect-fraud.html
[science]: https://towardsdatascience.com/benfords-law-in-the-gaia-universe-b5727db7a936
[quality of data]: https://www.idfcinstitute.org/blog/2020/november/using-benfords-law-to-understand-covid-19-data-quality/