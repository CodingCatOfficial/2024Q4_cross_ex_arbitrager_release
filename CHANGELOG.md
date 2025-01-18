# Update

## 2025-01-05

- add a new `stopping hedge condition` when net_position is large than 5*order qty
- update on error handling for bingx's get position amount api.

## 2024-12-18

- fix trading in dual position mode for bingx
- make a buffer for requesting bitget's order details to avoid empty response

## 2024-12-17

- update bitget's funding rate api to v2.
- debug ping-pong for binance's websocket.

## 2024-11-11

- add the alternative `1000XUSDT` for bybit

## 2024-10-27

- add messagebox to ask if start trading when initiate at inbalance positions.

## 2024-10-25

- some minor fixes.

## 2024-10-20

- set default recv_window to be 7.5 for bybit.
- unify the ex's names to lowercases.