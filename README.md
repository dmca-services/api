# DMCA.com [![DMCA API](https://images.dmca.com/Badges/dmca-badge-w200-5x1-04.png)](https://www.dmca.com)

The official documentation for DMCA services API.
Use the API to 
- [register an account](https://github.com/dmca-services/api/wiki/Register)
- [create a dmca takedown case](https://github.com/dmca-services/api/wiki/CreateCase)
- [list your dmca takedown cases](https://github.com/dmca-services/api/wiki/ListCases)
- [register an affiliate account](https://github.com/dmca-services/api/wiki/CreateACAccount-(Affiliate-Child))
- [create DIY cases](https://github.com/dmca-services/api/wiki/CreateCase)
- get a new badge id

## Usage Requirements

You must have an active account at https://www.dmca.com?r=ghapi

## Documentation

See the [API docs](https://github.com/dmca-services/api/wiki).


## API JS Example

<pre> function newRegistration(firstName, lastName, companyName, email, callBack) {
                var data = {
                        "FirstName": firstName,
                        "LastName": lastName,
                        "CompanyName": companyName,
                        "Email": email
                    };
                $.ajax({
                    type: "POST",
                    contentType: 'application/json; charset=utf-8',
                    url: "https://api.dmca.com/register",
                    data: JSON.stringify(data),
                    dataType: "json",
                    crossDomain: true,
                    context: this,
                    success: function (response) {
                        if (typeof callBack !== 'undefined') { callBack(response); }
                    }
                });
            }</pre>
