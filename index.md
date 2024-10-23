<html>
	<body>
		<script type='text/javascript'>
			function initEmbeddedMessaging() {
				try {
					embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'

					window.addEventListener("onEmbeddedMessagingReady", e => {
					  embeddedservice_bootstrap.prechatAPI.setVisiblePrechatFields({
					    // List the pre-chat field names with the value and whether
					    // it's editable in the pre-chat form.
					    	"Account_Code": {
					      "value": "AA1232",
					      "isEditableByEndUser": true
					    },
	 					"_email": {
					      "value": "Jane@testemail.com.invalid",
					      "isEditableByEndUser": true
					    }
	 				  });
					});
					embeddedservice_bootstrap.init(
						'00DRL000005cUNB',
						'NAT_Chat_Web',
						'https://fleetcorna--amznchat2.sandbox.my.site.com/ESWNATChatWeb1728151742952',
						{
							scrt2URL: 'https://fleetcorna--amznchat2.sandbox.my.salesforce-scrt.com'
						}
					);
				} catch (err) {
					console.error('Error loading Embedded Messaging: ', err);
				}
			};
		</script>
		<script type='text/javascript' src='https://fleetcorna--amznchat2.sandbox.my.site.com/ESWNATChatWeb1728151742952/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>
	</body>
</html>
