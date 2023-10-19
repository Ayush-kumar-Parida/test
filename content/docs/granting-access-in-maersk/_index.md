---
title : 'Granting Access in Maersk'
date : 2023-10-05T21:05:41+05:30
draft : false
weight : 2
---

Maersk.com allows a user to perform operations on a single customer. **The role issued to a customer grants the user privileges to perform an action.** This can be either to download a web bill of lading or make a booking. Maersk's authorisation server also needs to vet the relationship between the user and the customer the user is working on behalf of. **This relation is validated as part of the [KYC](## "Process businesses use to verify the identity of their customers or clients") process. The customer id is added as a [claim](## "Claims are assertions or statements about a user's identity that provide information about the user and their access rights") in a [stateless](## "System or architecture that does not retain information about the past interactions or states of users, clients, or sessions") token we pass downstream.** Later implementations have linked the customercode and scope together to provide more granular access.
