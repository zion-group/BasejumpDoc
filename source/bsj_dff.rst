########
DFF
########

*******
bsg_dff
*******

* Overview

  This dff is positive edge triggered,the cell provides three ports(clk_i,data_i,data_o).

- Interface
  
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

  width_p : input and output data width.

  harden_p

  strength_p : set drive strength.

- Application scenarios

  regfile

* Circuit structure
  
   .. image :: image/bsg_dff.jpg

***********
bsg_dff_en
***********

* Overview

  This dff is positive edge triggered, D-type flip-flop with active-high synchronous enable (en_i). The cell has a single output (data_o).

- Interface
  
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
  
  width_p : input and output data width.
  
  harden_p

  strength_p : set drive strength.

- Application scenarios

  clock gating control

* Circuit structure
  
   .. image :: image/bsg_dff_en.jpg

**************
bsg_dff_reset
**************

* Overview

  This dff is positive edge triggered, D-type flip-flop with active-high synchronous reset (reset_i). The cell has a single output (data_o).

- Interface
  
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
  
  width_p : input and output data width.
  
  harden_p

- Application scenarios

  pipeline register 

* Circuit structure
  
   .. image :: image/bsg_dff_reset.jpg

*****************
bsg_dff_reset_en
*****************

* Overview

  This dff is positive edge triggered, D-type flip-flop with active-high synchronous reset (reset_i) and active-high synchronous enable (en_i) . The cell has a single output (data_o).

- Interface

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
  
  width_p : input and output data width.

  harden_p

  reset_val_p : Bit extended reset_val_p is initial value of data_o after reset.

- Application scenarios

  

* Circuit structure
  
   .. image :: image/bsg_dff_reset_en.jpg

**********************
bsg_dff_negedge_reset
**********************

* Overview

  This dff is negative edge triggered, D-type flip-flop with active-high synchronous reset (reset_i). The cell has a single output (data_o).

- Interface
  
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
  
  width_p : input and output data width.
  
  harden_p

- Application scenarios

  

* Circuit structure
  
   .. image :: image/bsg_dff_negedge_reset.jpg

******************
bsg_dff_gatestack
******************

* Overview

  The cell provides three ports(i0,i1,o) and consists of  width_p flip-flops in parallel.This dff gatestack is positive edge of i1 triggered.

- Interface
  
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

  width_p : input and output data width.
  
  harden_p

- Application scenarios

  

* Circuit structure
  
   .. image :: image/bsg_dff_gatestack.jpg

******************
bsg_dff_chain
******************

* Overview

  The cell provides three ports(clk_i,data_i,data_o) and consists of  width_p serial `bsg_dff`_. This dff chain is positive edge  triggered.

- Interface
  
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

  width_p : input and output data width.

  num_stages_p : the number of `bsg_dff`_.

- Application scenarios

  

* Circuit structure
  
   .. image :: image/bsg_dff_chain.jpg
