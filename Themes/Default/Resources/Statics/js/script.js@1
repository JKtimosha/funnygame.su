$(function(){
	$('body').on('click', '.spoiler > .panel-heading > .spoiler-trigger', function(e){
		e.preventDefault();

		var spoiler = $(this).closest('.spoiler');

		spoiler.children('.spoiler-body').slideToggle('fast', function(){
			spoiler.toggleClass('toggle');
		});
	})
});