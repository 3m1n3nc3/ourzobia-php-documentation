#######################
Temporary Configuration
#######################

Temporary configuration were added in v1.1.5 to allow logged in admin users to quickly make changes to the site that will only have effects on the current session, this is especially useful if you have to test out a feature before making it publicly available. 

To use this feature add the following string to the end of the current url on the address bar and load the page: ``?config=true&config_setting=confg_value`` Where ``config_setting`` is the setting you want to change and ``config_value`` is the new value for the setting.

To clear a setting, simply set an empty value

Eg. ``http://yourdomain.com/admin/?config=true&site_theme=lite``

Available settings include:

===============================  ========================  ===============
Configuration                    config_setting            Possible Values
===============================  ========================  =============== 
Activation Email                 ``send_activation`` 	   [0],[1]
Admin Theme                      ``admin_theme``           [default]
Allow Crypto Currencies          ``allow_crypto``          [0],[1]
Allowed Crypto Wallets           ``allowed_wallets``       [bitcoin,litcoin]
Auto Pair Cashouts               ``auto_m_cashout``        [0],[1]
Auto Pair Pledges                ``auto_m_pledge``         [0],[1]
Block after timeout              ``block_timeout``         [0],[1]
Block Fraud Attempts             ``block_fraud``           [0],[1]
Comments per post                ``perppost``              [10] Any Nuumber
Countdown Time                   ``countdown_time``        [06:00:00]
Enforce Upgrade after            ``enforce_upgrade`` 	   [0],[1]
Enforce Recommitments            ``recommitment``          [0],[1]
Force Testimonies                ``force_testimony``       [0],[1]
Frontend Theme                   ``frontend_theme``        [default]
Google Analytics Key             ``google_analytics_key``  []
Inline Comments                  ``inline_comments``       [10] Any Nuumber or [0] to turn off
Min. Ref. Bonus Withdrawal       ``min_ref_withdraw``      [100]
Pagination Method                ``pagination``            [scroll],[click]
Paystack Public Key              ``paystack_public``       []
Paystack Secret Key              ``paystack_secret``       []
Posts per page                   ``perpage``               [10] Any Nuumber or [0] to turn off
Preferred Method to Fetch Banks  ``pref_fetch_bank_mode``  [api],[db]
Registration Mode                ``reg_mode``              [0],[1],[2]
Restrictions                     ``restrictions``          [0],[1],[2],[3]
Show Countdown                   ``show_countdown``        [0],[1]
Show Page Loader                 ``show_loader``           [0],[1]
Site Mode                        ``site_mode``             [0],[1],[2],[3]
Tawk.to Property ID              ``tawk_id``               []
Theme Mode                       ``theme_mode``            [dark],[light]
Timeout Action                   ``timeout_action``        [0],[1],[2],[3],[4],[5],[6],[7]
Token Lifespan                   ``token_lifespan``        [10] Any Nuumber
Welcome Email                    ``send_welcome``          [0],[1]
===============================  ========================  ===============

Caution should be exercised when using this feature, even though setting configuration this way will only affect the current session, you risk breaking your experience or in extreme rare but not impossible cases, could grant you access to break the site.
