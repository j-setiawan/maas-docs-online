Prepaid Subscriptions
======================

Prepaid subscriptions are a way to pay upfront for PubSub+ Cloud messaging services at a discounted price.
Subscriptions come with service and network data usage which are used by PubSub+ Cloud messaging services before
falling back to on-demand rates.

Details
~~~~~~~
Subscriptions are purchased with a set number of service usage months and GB of network data usage per month, typically a year at a time (i.e. 12 months).
At the beginning every month, each subscription is translated into the number of hours in the month for their given plan.
For example, 2 kilo subscriptions and 1 mega subscription in January is interpreted as 1488 hours of kilo services and 744 hours of mega services (31 days * 24 hours).
Each PubSub+ Cloud messaging service uses hours while it is running, rounded up to the nearest hour.

At the end of the month, the total number of service hours per plan and total network data usage are calculated.
For service usage, each subscription's included service usage reduces the total hours used of the respective plan.
For network data usage, each subscription's included network data usage is pooled together and reduces the total network data usage.
The remainder is charged at on-demand rates.

Unused subscription service and network data usage are not rolled over to the next month.

Example
~~~~~~~
Assume that the following subscriptions were purchased, each with 6 months of service:

- 2x kilo subscription with 50GB of network data usage
- 1x mega subscription with 200GB of network data usage

This means for 6 months, the following usage will be included without any extra cost per month:

- 2 * (24 * number of days in month) hours of kilo service usage (ex. 1488 hours for months with 31 days)
- (24 hours * number of days in month) hours of mega service usage (ex. 744 hours for months with 31 days)
- 300GB of network data usage (50GB x 2 for each kilo subscription + 200GB for mega subscription)

Suppose in January, the following services were created:

- Kilo service, running for the entire month, used 25GB of network data
- Kilo service, running for the entire month, used 100GB of network data
- Kilo service, running for the entire month, used 125GB of network data
- Mega service, running for half of the month, used 50GB of network data
- Mega service, running for half of the month, used 100GB of network data
- Giga service, running for 1 hour and 54 minutes, used 10GB of network data

At the end of the month, the usage is as follows:

- 2232 hours of kilo service usage (1 month of hours x 3 kilo services)
- 744 hours of mega service usage (0.5 month of hours x 2 mega services)
- 2 hours of giga service usage (1 hour and 54 minutes rounded up)
- 410GB of network data usage

After subtracting the included usage from the prepaid subscription, the following will be charged at the on-demand rates:

- 744 hours of kilo service usage (2232 kilo hours used - 1488 kilo hours from subscriptions)
- 0 hours of mega service usage (744 mega hours - 744 mega hours from subscription)
- 2 hours of giga service usage (2 giga hours - 0 giga hours from subscriptions)
- 110GB of network data usage (400GB used - 300GB network data usage from subscriptions)

Starting July, all usage will be considered on-demand usage unless subscriptions are purchased again.