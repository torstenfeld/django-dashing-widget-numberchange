django-dashing-widget-numberchange
==================================

Modified version of the default django-dashing number widget where value is compared to a previous value. Change is indicated through an icon.

![Numberchange Widget](http://i.imgur.com/TJk67bI.png)

## Usage

Add **numberchange** to [``INSTALLED_WIDGETS``](http://django-dashing.readthedocs.org/en/latest/getting-started.html#django-settings) and finally add the following code to your dashing [javascript configuration file](http://django-dashing.readthedocs.org/en/latest/getting-started.html#config-file).

    <dashboard>.addWidget('number_change_test_widget', 'Numberchange', {
        getData: function () {
            var self = this;
            $.extend(self.data, {
                title: 'Number change test',
                value: 5,
                previous: 7,
                updated_at: '6.1.2015 12:40:43'
            });
            home.publish('number_change_test_widget/render');
        }
    });

Replacing ``<dashboard>`` for your dashboard name.