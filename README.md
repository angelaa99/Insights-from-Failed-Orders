# Insights-from-Failed-Orders

## Background

Gett, previously known as GetTaxi, is an Israeli-developed technology platform solely focused on corporate Ground Transportation Management (GTM). They have an application where clients can order taxis, and drivers can accept their rides (offers). At the moment, when the client clicks the Order button in the application, the matching system searches for the most relevant drivers and offers them the order. 

## Objective

To investigate some matching metrics for orders that did not completed successfully, i.e., the customer didn't end up getting a car.

## Data Description

The data set `data_orders` is stored in CSV format. The columns in the `data_orders` are as follows:

- `order datetime` = order time 
- `origin longitude` = order longitude 
- `origin latitude` = order latitude
- `order gk` = order number 
- `m order eta` = time before order arrival
- `order status key` = status, an enumeration of the following mappings:
    - 4 (canceled by the client), 
    - 9 (canceled by the system, indicating a rejection)
- `is_driver assigned key` = whether or not a driver has been assigned 
- `cancellation time in seconds` = the number of seconds that passed before cancellation

The `data_offers` data set is a simple map with 2 columns:
- `order_gk` - order number, associated with the same column from the `orders` data set
- `offer_id` - ID of an offer
