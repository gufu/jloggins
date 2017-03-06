jloggins
========

A simple console logging utility for JQuery

	<script type="text/javascript">
		//Logging is off by default you must set the level to see it
		// Use the javascript console or hard code the level in code somewhere, preferably before any other logging is executed
		$.log.level('all'); //How much logging do you want to see
		//  'all' 'debug' 'info' 'warn' 'error' 'none'
		
		$.log.write('Celebrate Me Home'); 
        //> Celebrate Me Home
        
        
        $.log.debug('Nightwatch');
        //>[+] Night Watch
        
        
        $.log.info('Keep the Fire');
        //>[?] Keep the Fire
        
        
        $.log.warn('High Adventure');
        //>[*] High Adventure
        
        
        $.log.error('Leap of Faith');
        //>[!] Leap of Faith
        
        
        try	{
            	throw new Error('I Believe in Love')
            }
        catch(e) {
        		$.log.exception(e);
            }
        //>[!] 1351 : I Believe in Love
        
        
        $.log.enter('If You Believe'); //Enters a contextual code block
        $.log.debug('All Join In'); //Message will appear with contextual note
        //>[!] If You Believe : All Join In
        $.log.exit(); //Exits a contextual code block
        
        
        $.log.start('It\'s About Time'); //Enters a timed code block
        //Something that takes time
        $.log.stop(); //Exits and prints duration along with title
        // It's About Time 0:5:295
        
        
        $.log.reset(); //Clears context and timer stack
        
        
        $(this).log().info('How About Now'); //Writes message with (this) as
        // [?] A #mylink .myClass : How About Now
        
        
        $(this).log().warn('How About Now'); //Writes message with (this) as
        // [*] A #mylink .myClass : How About Now
        
        
        $(this).log().error('How About Now'); //Writes message with (this) as
        // [!] A #mylink .myClass : How About Now
        
        
        $.log.info('arguments','are','concatenated')
        // [?] arguments are concatenated
        
        
        var why = 'why';
        var should = 'should'
        $.log.info(why,' ',should,' I care')
        // [?] why should I care
	</script>