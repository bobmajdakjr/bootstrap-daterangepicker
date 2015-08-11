# Date Range Picker for Bootstrap

For the most part this fork is the same as the original source found on  [dangrossman/bootstrap-dateragepicker](https://github.com/dangrossman/bootstrap-daterangepicker) so the bulk of the credit goes to him and the things you can find in his README.md.

It currently adds one feature that was denied for merge.

### Event: before.daterangepicker
Allows you to modify the picker before it tries to use its own data to render itself, with ease, and inline with execution. My use case was our date range is two fields, and for various reasons we just didn't want to use the range selection for ease of the UI by the common user.

	InputStart
	.daterangepicker(DateOpt)
	.on('before.daterangepicker',function(e,picker){
		// make sure all the days after date-end are greyed out.
		picker.maxDate = moment(InputEnd.val(),picker.locale.format);
	});


