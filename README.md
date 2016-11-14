# vertx-eventbus-plus

vertx eventbux plus

Enhancements:

- auto reconnect (2016/11/14)

Usage:

```javascript

	var eventBus = new EventBus('server url', {
	    reconnectionAttempts: 5,
	    reconnectionDelay: 5000 	
	});
	
	eventBus.onopen = function() {
	    ...
	}
	
	eventBus.onerror = function() {
	    ...
	}
	
	eventBus.onclose = function() {
	    ...
	}
	
	// emit after 5 attempts of reconnection
	eventBus.onfatal = function(e) {
	    console.error(e);
	}

```