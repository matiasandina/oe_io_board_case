This repository contains the files to cut a case for the Open Ephys Input Output board.
There are two versions of files, one for the regular IO board, and another for a IO board combined with a db25 terminal block.

## Open Ephys IO Case

This is a simple project based on 2 layer acrylic that is laser cut using files. The main motivation is to go from this classical cardboard + tape approach:

![](/img/06.jpg)

To this slightly better version:

![](/img/07.jpg)

This plays nicely with the Acquisition Board

![](/img/08.jpg)

### Materials

* M3 15 or 20 mm bronze standoffs.
* Laser cut case. Files found in this repository.

## Open Ephys IO + db25 Case

This project used a generic db25 terminal block and might need to be adjusted. See [here](https://www.amazon.com/Connector-D-sub-25-pin-Terminal-Breakout/dp/B073RG3GG6/ref=asc_df_B073RG3GG6/?tag=hyprod-20&linkCode=df0&hvadid=216539509836&hvpos=&hvnetw=g&hvrand=17758274187648212718&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9002000&hvtargid=pla-348800028947&psc=1) for the link.
We also used a male-female db25 cable (such as [this one](https://www.amazon.com/dp/B092QWDZQZ/ref=twister_B092QTYJWY?_encoding=UTF8&th=1)) to connect the db25 terminal into a TDT RZ10X system.

This provided 8 digital and could be expanded by wiring extra channels to another IO board if needed.
An additional advantage is the use of a single cable (the db25 male-female) instead of multiple BNC cables at the input of the RZ10X, which makes things cleaner.

The pinout for the TDT can be found [here](https://www.tdt.com/docs/hardware/rz10-lux-integrated-processor/#db25-digital-io-pinout) and reproduced below.

![](https://www.tdt.com/docs/hardware/assets/images/RZ_DB25_DigitalIO_PO.png)

### Materials

* M3 20 mm bronze standoffs
* 2 precision screwdrivers for the terminals
* Phoenix style 10 position terminal blocks. We bought 10 instead of 9 because it was easier to get the generic parts from [here](https://www.amazon.com/Augiimor-15PCS-2-54mm-Terminal-Connector/dp/B08B3P8BF3/ref=sr_1_1?content-id=amzn1.sym.ea945d40-8e84-42be-ad5c-249b9bca6a40%3Aamzn1.sym.ea945d40-8e84-42be-ad5c-249b9bca6a40&crid=LO0KLJ0QGMNO&keywords=Terminal+Blocks&pd_rd_r=34f6a4ff-55dc-4279-a9ce-c62dfcd055c4&pd_rd_w=BgHsc&pd_rd_wg=q5rzY&pf_rd_p=ea945d40-8e84-42be-ad5c-249b9bca6a40&pf_rd_r=XCCGPE5VDCCF3R8Z1M9B&pid=rYagDl8&qid=1677857597&refinements=p_n_feature_thirteen_browse-bin%3A18945667011&s=industrial&sprefix=2.54%2Bmm%2Bmount%2Bterminal%2Bblock%2Ctools%2C73&sr=1-1)
* Soldering iron and misc
* 22 AWG wires
* Tape
* Laser cut case. Files found in this repository.

### Assembly

Solder the phoenix-style terminal blocks to the Open Ephys Input Output board. To make things cleaner, we soldered with the exits looking "inward". Later on, add standoffs to the acrylic base layer

![](/img/01.jpg)

Position the boards and follow the channel map according to the pinout that you want to use. You can use some tape to make things tidier.

![](/img/02.jpg)

Position the standoffs for the second layer and put the acrylic top. You might need to wiggle things if the fit is too tight.

![](/img/03.jpg)

![](/img/04.jpg)

Test the device is working by connecting to your db25 source. In our case, this was a TDT RZ10X, which has a minimal current when idle.

![](/img/output.gif)

This is a minimal test, you should test that channels are independent by sending pulses in/out of your devices!

## Contribute

This is release of open hardware is 'as is'. If you improve it or build upon it, please file issues or PR to contribute to the community.
