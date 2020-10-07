<style type='text/css'>
	.embeddedServiceHelpButton .helpButton .uiButton {
		background-color: #006DA4;
		font-family: “Proxima Nova”, sans-serif;
	}
	.embeddedServiceHelpButton .helpButton .uiButton:focus {
		outline: 1px solid #006DA4;
	}
</style>
<script type=‘text/javascript’ src=’https://service.force.com/embeddedservice/5.0/esw.min.js'></script>
<script type=‘text/javascript’>
	var initESW = function(gslbBaseURL) {
		embedded_svc.settings.displayHelpButton = true; //Or false
		embedded_svc.settings.language = ‘’; //For example, enter ‘en’ or ‘en-US’
		//embedded_svc.settings.defaultMinimizedText = ‘...‘; //(Defaults to Chat with an Expert)
		//embedded_svc.settings.disabledMinimizedText = ‘...‘; //(Defaults to Agent Offline)
		//embedded_svc.settings.loadingText = ‘’; //(Defaults to Loading)
		//embedded_svc.settings.storageDomain = ‘yourdomain.com’; //(Sets the domain for your deployment so that visitors can navigate subdomains during a chat session)
		// Settings for Chat
		//embedded_svc.settings.directToButtonRouting = function(prechatFormData) {
			// Dynamically changes the button ID based on what the visitor enters in the pre-chat form.
			// Returns a valid button ID.
		//};
		//embedded_svc.settings.prepopulatedPrechatFields = {}; //Sets the auto-population of pre-chat form fields
		//embedded_svc.settings.fallbackRouting = []; //An array of button IDs, user IDs, or userId_buttonId
		//embedded_svc.settings.offlineSupportMinimizedText = ‘...’; //(Defaults to Contact Us)
		embedded_svc.settings.enabledFeatures = [‘LiveAgent’];
		embedded_svc.settings.entryFeature = ‘LiveAgent’;
		embedded_svc.init(
			’https://crocs.my.salesforce.com',
			’https://crocs.secure.force.com/chat',
			gslbBaseURL,
			‘00D60000000KGaJ’,
			‘Bogus_Einstein_Bot’,
			{
				baseLiveAgentContentURL: ’https://c.la4-c2-ph2.salesforceliveagent.com/content',
				deploymentId: ‘5723u000000lOXd’,
				buttonId: ‘5733u000000lAvf’,
				baseLiveAgentURL: ’https://d.la4-c2-ph2.salesforceliveagent.com/chat',
				eswLiveAgentDevName: ‘EmbeddedServiceLiveAgent_Parent04I3u0000004EyyEAE_17307076fb5’,
				isOfflineSupportEnabled: false
			}
		);
	};
	if (!window.embedded_svc) {
		var s = document.createElement(‘script’);
		s.setAttribute(‘src’, ’https://crocs.my.salesforce.com/embeddedservice/5.0/esw.min.js');
		s.onload = function() {
			initESW(null);
		};
		document.body.appendChild(s);
	} else {
		initESW(’https://service.force.com');
	}
</script>
