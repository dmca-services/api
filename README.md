# DMCA.com [![DMCA API](https://images.dmca.com/Badges/dmca-badge-w200-5x1-04.png)](https://www.dmca.com)
See the [API docs](https://app.swaggerhub.com/apis-docs/dmca/dmca-api/2.1.1)

The official documentation for DMCA services API.
Use the API to 
- [register an account](https://app.swaggerhub.com/apis-docs/dmca/dmca-api/2.1.1#/Public%20API/%2Fregister%2Fpost)
- [login to API and get your token](https://app.swaggerhub.com/apis-docs/dmca/dmca-api/2.1.1#/Public%20API/%2Flogin%2Fpost)
- [create a dmca takedown case](https://app.swaggerhub.com/apis-docs/dmca/dmca-api/2.1.1#/DMCA%20Takedowns%20Public%20API/%2FcreateCase%2Fpost)
- [list your dmca takedown cases](https://app.swaggerhub.com/apis-docs/dmca/dmca-api/2.1.1#/DMCA%20Takedowns%20Public%20API/%2FlistCases%2Fget)
- [register an affiliate account](https://app.swaggerhub.com/apis-docs/dmca/dmca-api/2.1.1#/DMCA.com%20Affiliate/%2FregisterAffiliate%2Fpost)
- [create DIY cases](https://app.swaggerhub.com/apis-docs/dmca/dmca-api/2.1.1#/DMCA%20DIY%20Cases/%2FcreateDIYCase%2Fpost)
- get a new badge id

## Usage Requirements

You must have an active account at https://www.dmca.com?r=ghapi

## Documentation

See the [API docs](https://app.swaggerhub.com/apis-docs/dmca/dmca-api/2.1.1).


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
