# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

<!-- next-header -->
## Unreleased - ReleaseDate

- Added OPEN Alliance TC6 SPI protocol support (ADIN2111 in OPEN Alliance SPI mode)
- Added port aware raw frame I/O for the ADIN2111 in OPEN Alliance TC6 mode: `new_tc6_port_io` returns a
  `PortIo` that selects the egress port per frame and reports the ingress port of each received frame,
  for consumers that do not use embassy-net. `Tc6::send_frame_to`, `Tc6::read_frame_port`,
  `ADIN1110::write_fifo_to` and `ADIN1110::read_fifo_port` expose the same on the lower layers, and
  `MDIO_PHY_ADDR_PORT2` is now public. The existing `new`, `new_tc6`, `Device` and `Runner::run` paths
  are unchanged.

## 0.4.0 - 2026-03-10

- Update embassy-net-driver-channel to 0.4.0

## 0.3.1 - 2025-08-26

- First release with changelog.
