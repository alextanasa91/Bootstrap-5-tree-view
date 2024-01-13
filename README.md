    $.ajax({
        async: false,
            type: "GET",
            url: "<?=base_url("categorii/listeaza");?>",
            datatype: "json",
            success: function(data){
                result = JSON.parse(data);
            }
    });
    
		$('#tree').bstreeview({ 
			data: result,
      expandIcon: 'fa fa-angle-down fa-fw',
      collapseIcon: 'fa fa-angle-right fa-fw',
      indent: 1.25,
      parentsMarginLeft: '1.25rem',
		});
