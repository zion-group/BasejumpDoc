########
bsg_misc
########

This section introduces all kinds of Dffs provided in bsg library.

********
bsg_dff
********

* Overview

  This dff is positive edge triggered with no reset.

- Port
  
  +---------+---------+----------+---------------------------------------------+
  |         |   NAME  |   WIDTH  |    DESCRIPTION                              |
  +---------+---------+----------+---------------------------------------------+ 
  |  CLOCK  |  clk_i  |     1    | clock port                                  |
  +---------+---------+----------+---------------------------------------------+
  |  INPUT  | data_i  | width_p  | data input port                             |
  +---------+---------+----------+---------------------------------------------+
  | OUTPUT  | data_o  | width_p  | data output port                            |
  +---------+---------+----------+---------------------------------------------+

* Parameter

  +------------+-------------------------------------------------------------------+ 
  |  width_p   | input and output data width                                       |
  +------------+-------------------------------------------------------------------+
  |  harden_p  | use harden IP or not                                              |
  +------------+-------------------------------------------------------------------+
  | strength_p | set drive strength                                                |
  +------------+-------------------------------------------------------------------+

- Assertion
  
  None
  
* Circuit structure
  
   .. image :: image/bsg_dff.jpg

***********
bsg_dff_en
***********

* Overview

  This dff is positive edge triggered, D-type flip-flop with active-high synchronous enable.

- Port
  
  +---------+---------+----------+--------------------------------------------+
  |         |   NAME  |   WIDTH  |                 DESCRIPTION                |
  +---------+---------+----------+--------------------------------------------+ 
  |  CLOCK  |  clk_i  |     1    | clock port                                 |
  +---------+---------+----------+--------------------------------------------+
  |         | data_i  | width_p  | data input port                            |
  +  INPUT  +---------+----------+--------------------------------------------+
  |         |  en_i   |     1    | enable port                                |
  +---------+---------+----------+--------------------------------------------+
  | OUTPUT  | data_o  | width_p  | data output port                           |
  +---------+---------+----------+--------------------------------------------+

* Parameter
  
  +------------+-------------------------------------------------------------------+ 
  |  width_p   | input and output data width                                       |
  +------------+-------------------------------------------------------------------+
  |  harden_p  | use harden IP or not                                              |
  +------------+-------------------------------------------------------------------+
  | strength_p | set drive strength                                                |
  +------------+-------------------------------------------------------------------+

- Assertion
  
  None

* Circuit structure
  
   .. image :: image/bsg_dff_en.jpg

**************
bsg_dff_reset
**************

* Overview

  This dff is positive edge triggered, D-type flip-flop with active-high synchronous reset.

- Port
  
  +---------+---------+----------+--------------------------------------------+
  |         |   NAME  |   WIDTH  |                 DESCRIPTION                |
  +---------+---------+----------+--------------------------------------------+ 
  |  CLOCK  |  clk_i  |     1    | clock port                                 |
  +---------+---------+----------+--------------------------------------------+
  |  RESET  | reset_i |     1    | reset port                                 |
  +---------+---------+----------+--------------------------------------------+
  |  INPUT  | data_i  | width_p  | data input port                            |
  +---------+---------+----------+--------------------------------------------+
  | OUTPUT  | data_o  | width_p  | data output port                           |
  +---------+---------+----------+--------------------------------------------+

* Parameter
  
  +------------+-------------------------------------------------------------------+ 
  |  width_p   | input and output data width                                       |
  +------------+-------------------------------------------------------------------+
  |  harden_p  | use harden IP or not                                              |
  +------------+-------------------------------------------------------------------+

- Assertion
  
  None
  
* Circuit structure
  
   .. image :: image/bsg_dff_reset.jpg

*****************
bsg_dff_reset_en
*****************

* Overview

  This dff is positive edge triggered, D-type flip-flop with active-high synchronous reset and active-high synchronous enable.

- Port

  +---------+---------+----------+--------------------------------------------+
  |         |   NAME  |   WIDTH  |                 DESCRIPTION                |
  +---------+---------+----------+--------------------------------------------+ 
  |  CLOCK  |  clk_i  |     1    | clock port                                 |
  +---------+---------+----------+--------------------------------------------+
  |  RESET  | reset_i |     1    | reset port                                 |
  +---------+---------+----------+--------------------------------------------+
  |         | data_i  | width_p  | data input port                            |
  +  INPUT  +---------+----------+--------------------------------------------+
  |         |  en_i   |     1    |  enable port                               |
  +---------+---------+----------+--------------------------------------------+
  | OUTPUT  | data_o  | width_p  | data output port                           |
  +---------+---------+----------+--------------------------------------------+

* Parameter
  
  +------------+-------------------------------------------------------------------+ 
  |  width_p   | input and output data width                                       |
  +------------+-------------------------------------------------------------------+
  |  harden_p  | use harden IP or not                                              |
  +------------+-------------------------------------------------------------------+
  | reset_val_p| Bit extended reset_val_p is initial value of data_o after reset   |
  +------------+-------------------------------------------------------------------+

- Assertion

  None

* Circuit structure
  
   .. image :: image/bsg_dff_reset_en.jpg

**********************
bsg_dff_negedge_reset
**********************

* Overview

  This dff is negative edge triggered, D-type flip-flop with active-high synchronous reset.

- Port
  
  +---------+---------+----------+--------------------------------------------+
  |         |   NAME  |   WIDTH  |                 DESCRIPTION                |
  +---------+---------+----------+--------------------------------------------+ 
  |  CLOCK  |  clk_i  |     1    | clock port                                 |
  +---------+---------+----------+--------------------------------------------+
  |  RESET  | reset_i |     1    | reset port                                 |
  +---------+---------+----------+--------------------------------------------+
  |  INPUT  | data_i  | width_p  | data input port                            |
  +---------+---------+----------+--------------------------------------------+
  | OUTPUT  | data_o  | width_p  | data output port                           |
  +---------+---------+----------+--------------------------------------------+

* Parameter
  
  +------------+-------------------------------------------------------------------+ 
  |  width_p   | input and output data width                                       |
  +------------+-------------------------------------------------------------------+
  |  harden_p  | use harden IP or not                                              |
  +------------+-------------------------------------------------------------------+

- Assertion

  None

* Circuit structure
  
   .. image :: image/bsg_dff_negedge_reset.jpg

******************
bsg_dff_gatestack
******************

* Overview

  The cell provides three ports(i0,i1,o) and consists of width_p flip-flops in parallel.This dff gatestack is positive edge of i1 triggered.

- Port
  
  +---------+---------+----------+---------------------------------------------+
  |         |   NAME  |   WIDTH  |    DESCRIPTION                              |
  +---------+---------+----------+---------------------------------------------+ 
  |         |    i0   | width_p  | data input port                             |
  +  INPUT  +---------+----------+---------------------------------------------+
  |         |    i1   | width_p  | data transmission trigger port              |
  +---------+---------+----------+---------------------------------------------+
  | OUTPUT  |    o    | width_p  | data output port                            |
  +---------+---------+----------+---------------------------------------------+

* Parameter

  +------------+-------------------------------------------------------------------+ 
  |  width_p   | input and output data width                                       |
  +------------+-------------------------------------------------------------------+
  |  harden_p  | use harden IP or not                                              |
  +------------+-------------------------------------------------------------------+

- Assertion
  
  None

* Circuit structure
  
   .. image :: image/bsg_dff_gatestack.jpg

******************
bsg_dff_chain
******************

* Overview

  Chain several Dffs together. A Dff chain consists of  width_p serial `bsg_dff`_. It is positive edge triggered.

- Port
  
  +---------+---------+----------+---------------------------------------------+
  |         |   NAME  |   WIDTH  |    DESCRIPTION                              |
  +---------+---------+----------+---------------------------------------------+ 
  |  CLOCK  |  clk_i  |     1    | clock port                                  |
  +---------+---------+----------+---------------------------------------------+
  |  INPUT  | data_i  | width_p  | data input port                             |
  +---------+---------+----------+---------------------------------------------+
  | OUTPUT  | data_o  | width_p  | data output port                            |
  +---------+---------+----------+---------------------------------------------+

* Parameter

  +------------+-------------------------------------------------------------------+ 
  |  width_p   | input and output data width.                                      |
  +------------+-------------------------------------------------------------------+ 
  |num_stages_p| stage number of `bsg_dff`_                                        |
  +------------+-------------------------------------------------------------------+

- Assertion

  None

* Circuit structure
  
   .. image :: image/bsg_dff_chain.jpg
