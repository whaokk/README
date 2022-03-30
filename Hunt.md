/**********************多语言************************/
		if (languageType == "en") {
					
				}
				else {
					
				}
				if (cc.sys.isBrowser) {
	var url = window.location.href;
	var loc = url.substring(url.lastIndexOf('languages=') + 10, url.length);
	Utils.language_type = loc;
	console.log('Utils.language_type  loc : ', Utils.language_type);
}
/**********************多语言************************/