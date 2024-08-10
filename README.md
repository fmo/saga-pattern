# Whats Saga
A saga is a sequence of local transactions that updates each service and publishes another message to trigger another local transaction on the next service.

# Type of Sagas

* Choreography-based Saga
* Orchestrator-based Saga

## Orchestration

There is a orchestrator and participants. Lets say there is an Order service which is the orchestrator and its communicating with Payment, Inventory and Shipping services.
If order service gets the successful payment first and deduct the inventory for the purchased product but Shipping service fails. 
Then there has to be a compensation transaction should be triggered by Order service. Which returns the product to inventory and refund the payment.
