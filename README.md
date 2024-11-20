To use a date picker in Magento 2, you can:
Create a system.xml 
Create a DatePicker class in the DatePicker.php file 
Add a field name, such as "example-date" 
Add the following JavaScript code after the closing tag: 
Code
```html
  <script>
  require([ 'jquery', 'mage/translate', 'mage/calendar' ], function ($, $t) {
  $('#example-date').calendar({
  changeMonth: true,
  changeYear: true,
  showButtonPanel: true,
  currentText: $t('Go Today'),
  closeText: $t('Close'),
  showWeek: true,
  showOn: "both",
  showsTime: true
  });
  </script>
```
You can also create custom classes to achieve multi-date selection functionality. One class should be a frontend model class to show the grid in the system configuration in admin, and the other should be a backend model class to save data in the database. 
The datepicker will open in a small overlay when the field is focused, and will close automatically when the field is blurred or a date is selected. 
