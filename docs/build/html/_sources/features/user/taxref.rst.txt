#########################
Maintenance
#########################

For a system to be sustainable there has to be features in place to make users give back to the community and that malicious actors are kept at bay, this is where our system maintenance features comes into play, we have put in various tools to ensure that users are always giving back to the system to avoid quick bankruptcy and also keep malicious people at bay.
Lets look at some of those features.

Tax
===

Our tax systems allows admin to set an amount or a percentage that is added to a user's accrued taxes for each successful cashout they make on the system, the accrued tax can then be collected by setting the :doc:`Control Configuration </config/control>` ``Enforce Tax`` and ``Tax Force Cap`` flags

Activation Fees
===============

The system allow you to set whether users should pay an activation fee, activation fees also help to keep the system healthy and free of malicious actors who may drain the system with face referral registrations. You can set the :doc:`Control Configuration </config/control>` ``Activation Fee`` and ``Pay activation fee to`` flags to activate and determine if activation fees come to admin or goes back to the community.

Reactivation Fees
=================

Reactivation fees are similar to Activation fees, the major difference is that Reactivation fees are collected as default fines for when users and caught by the systems spam bots or if they are reported, and found guilty of refusing to make payments in redemption of their pledges or refusing to confirm a user who makes payment. You can set the :doc:`Control Configuration </config/control>` ``Reactivation Fee (Fines)`` and ``Pay activation fee to`` flags to activate.

Monthly Reactivation Fees
=========================

Monthly Reactivation fees are similar to Activation fees and Reactivation fees, the major difference is that the Monthly Reactivation fees are collected from every user every month as maintenance fee for the system. You can set the :doc:`Control Configuration </config/control>` ``Monthly Reactivation Fee`` and ``Pay activation fee to`` flags to activate.

Referral Bonuses
================

Referral bonuses serve as incentives to users who are active in community building, when a user's referral link is used during registration, every investment made by the users referrals will return a percentage to them. Referral bonuses are active by default but you can set the :doc:`Control Configuration </config/control>` ``Min. Ref. Bonus Withdrawal`` and ``Last Pledge = Withdrawable Bonus`` flags to manage how bonuses a disbursed and withdrawn. The bonuses can be managed from the :doc:`Packages </features/admin/packages>` 