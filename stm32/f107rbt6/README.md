## STM32F107RBT6
This custom board contains: LAN8720A, PoE support.

### Enable Ethernet on Connectivity.
Configure `Parameter Settings`(`ETH` in `Connectivity` page) like:

* Mode: `RMII`.
* Ethernet Media Configuration: as your wish.
* Ethernet MAC Address: set anything except `00:00:00:00:00:00`.
* PHY Address Value: `0` (this is important!)

And then, enable `LWIP` to test the board's ethernet operational:
(This is located at `Middleware`)
* Check `Enabled` on `LWIP`.
* `LWIP_ICMP` on `General Settings`: Enabled. <-- `ping` command is based on `ICMP` traffic.
* `MEM_SIZE` on `Key Options`: `10 * 1600`. (Optional)

### Pin Mapping.
To enable this chip functionality, configure `RMII`:

* RCC: 8MHz.
* PC1: ETH_MDC
* PA1: ETH_REF_CLK
* PA2: ETH_MDIO
* PA7: ETH_CRS_DV
* PC4: ETH_RXD0
* PC5: ETH_RXD1
* PB10: ETH_RX_ER
* PB11: ETH_TX_EN
* PB12: ETH_TXD0
* PB13: ETH_TXD1
* PA11: USB_OTG_FS_DM
* PA12: USB_OTG_FS_DP

### LAN8720A.
STM32CubeIDE supports only `LAN8742A` but, `LAN8720A` is available with few changes.
Configure `Advanced Parameters`(`ETH` in `Connectivity` page) like:

* PHY: `LAN8742A_PHY_ADDRESS`
* Transceiver Basic Control Register: `0x00`
* Transceiver Basic Status Register: `0x01`
* PHY special control/status register Offset: `0x1f`
* PHY interrupt source flag register Offset: `0x001d`
* PHY Link down interrupt: `0x0010`

When if `PHY Address Value` is not editable even though this changed on `Parameter Settings`,
This can be modified by header file: `stm32f1xx_hal_conf.h` on `Core/Inc` directory.

```
......
/* Section 2: PHY configuration section */

/* LAN8742A_PHY_ADDRESS Address*/
// #define LAN8742A_PHY_ADDRESS         0x1U    // <-- comment this.
#define LAN8742A_PHY_ADDRESS            0x0U    // <-- set `PHY_ADDRESS` here

......
```

Then, you can program the board supports `10/100 Mbps Ethernet`.