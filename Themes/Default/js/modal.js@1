$(function(){

	$('body').on('click', '[data-modal]', function(e){
		if(e.target.tagName != 'INPUT'){
			e.preventDefault();
		}

		var that = $(this);

		var id = that.attr('data-modal');

		var modal = $('.modal[data-id="'+id+'"]');

		if(modal.length){

			if(id == 'paymodal'){
				modal.find('.modal-header').html('Покупка товара "'+that.children('.title').html()+'"');
				modal.find('[type="submit"]').html('Купить за '+that.children('.price').html());
				modal.find('[name="item_id"]').val(that.find('input[name="item_id"]').val());
				if(that.find('[name="amounted"]').val() == '1'){
					$('#amounted').show();
				}else{
					$('#amounted').hide();
				}
			}

			modal.fadeIn('fast', function(){
				$(this).addClass('active');
			});
		}
	}).on('click', '.modal [data-modal-close]', function(e){
		e.preventDefault();

		$('.modal').fadeOut('fast', function(){
			$(this).removeClass('active');
		});
	}).on('click', '.modal', function(e){
		var target = $(e.target);
		if(!target.closest('.modal-content').length){
			$('.modal').fadeOut('fast', function(){
				$(this).removeClass('active');
			});
		}
	});
});