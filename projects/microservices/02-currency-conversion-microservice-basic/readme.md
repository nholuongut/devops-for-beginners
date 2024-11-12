# Currency Conversion Micro Service

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>

Run com.nholuongut.microservices.currencyconversionservice.CurrencyConversionServiceApplication as a Java Application.

## Resources

- http://localhost:8100/currency-conversion/from/EUR/to/INR/quantity/10

```json
{
id: 10002,
from: "EUR",
to: "INR",
conversionMultiple: 75,
quantity: 10,
totalCalculatedAmount: 750
}
```

## Containerization

### Troubleshooting

- Problem - Caused by: com.spotify.docker.client.shaded.javax.ws.rs.ProcessingException: java.io.IOException: No such file or directory
- Solution - Check if docker is up and running!
- Problem - Error creating the Docker image on MacOS - java.io.IOException: Cannot run program “docker-credential-osxkeychain”: error=2, No such file or directory
- Solution - https://medium.com/@dakshika/error-creating-the-docker-image-on-macos-wso2-enterprise-integrator-tooling-dfb5b537b44e

### Creating Containers

- mvn package

### Running Containers

```
docker run --publish 8100:8100 --network currency-network --env CURRENCY_EXCHANGE_URI=http://currency-exchange:8000 in28min/currency-conversion:0.0.1-SNAPSHOT
```

#### Test API 
- http://localhost:8100/currency-conversion/from/EUR/to/INR/quantity/10

```
docker login
docker push @@@REPO_NAME@@@/currency-conversion:0.0.1-SNAPSHOT
```

#### Environment Variable

```
        env:     #CHANGE
          - name: CURRENCY_EXCHANGE_URI
            valueFrom:
              configMapKeyRef:
                key: CURRENCY_EXCHANGE_URI
                name: currency-exchange-uri-demo
```

## 🚀 I'm are always open to your feedback.  Please contact as bellow information
![](https://i.imgur.com/waxVImv.png)
# **[Contact Me]**
* [Name: Nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)
* [PayPal.Me](https://www.paypal.com/paypalme/nholuongut)

![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

![](https://i.imgur.com/waxVImv.png)
# License
* Nho Luong (c). All Rights Reserved.🌟
