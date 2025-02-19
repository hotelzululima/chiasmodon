
# Chiasmodon
[![asciicast](https://asciinema.org/a/W3jCmEetvRT6JjrBVDyKtSfbg.svg)](https://asciinema.org/a/W3jCmEetvRT6JjrBVDyKtSfbg)

Chiasmodon is an OSINT (Open Source Intelligence) tool designed to assist in the process of gathering information about a target domain. Its primary functionality revolves around searching for domain-related data, including domain emails, domain credentials (usernames and passwords), CIDRs (Classless Inter-Domain Routing), ASNs (Autonomous System Numbers), and subdomains. the tool allows users to search by domain, CIDR, ASN, email, username, password, or Google Play application ID. 



## ✨Features

- [x] **🌐Domain**: Conduct targeted searches by specifying a domain name to gather relevant information related to the domain.
- [x] **🎮Google Play Application**: Search for information related to a specific application on the Google Play Store by providing the application ID.
- [x] **🔎CIDR and 🔢ASN**: Explore CIDR blocks and Autonomous System Numbers (ASNs) associated with the target domain to gain insights into network infrastructure and potential vulnerabilities.
- [x] **✉️Email, 👤Username, 🔒Password**: Conduct searches based on email, username, or password to identify potential security risks or compromised credentials.
- [x] **📋Output Customization**: Choose the desired output format (text, JSON, or CSV) and specify the filename to save the search results.
- [x] **⚙️Additional Options**: The tool offers various additional options, such as viewing different result types (credentials, URLs, subdomains, emails, passwords, usernames, or applications), setting API tokens, specifying timeouts, limiting results, and more.


## 🚀Comping soon

- **📱Phone**: Get ready to uncover even more valuable data by searching for information associated with phone numbers. Whether you're investigating a particular individual or looking for connections between phone numbers and other entities, this new feature will provide you with valuable insights.

- **🏢Company Name**: We understand the importance of comprehensive company research. In our upcoming release, you'll be able to search by company name and access a wide range of documents associated with that company. This feature will provide you with a convenient and efficient way to gather crucial information, such as legal documents, financial reports, and other relevant records.

- **👤Face (Photo)**: Visual data is a powerful tool, and we are excited to introduce our advanced facial recognition feature. With "Search by Face (Photo)," you can upload an image containing a face and leverage cutting-edge technology to identify and match individuals across various data sources. This will allow you to gather valuable information, such as social media profiles, online presence, and potential connections, all through the power of facial recognition.

## Why Chiasmodon name ?
Chiasmodon niger is a species of deep sea fish in the family Chiasmodontidae. It is known for its ability to **swallow fish larger than itself**. and so do we. 😉
![Chiasmodon background](https://journal.voca.network/wp-content/uploads/2017/10/DTR083_1200.png)

## 🔑 Subscription
Join us today and unlock the potential of our cutting-edge OSINT tool. Contact https://t.me/Chiasmod0n on Telegram to subscribe and start harnessing the power of Chiasmodon for your domain investigations.

## Install
```bash
pip install chiasmodon
```
## 💻Usage
Chiasmodon provides a flexible and user-friendly command-line interface and python library. Here are some examples to demonstrate its usage:


***How to use pychiasmodon library***:
```python
from pychiasmodon import Chiasmodon as ch 
token = "PUT_HERE_YOUR_API_KEY"
obj = ch(token)
```

- **Searching for a target domain**:
    - *Command line*
        ```bash
        chiasmodon_cli.py --domain example.com
        ```
    - *Python*
        ```python
        result = obj.search('example.com',method='domain')
        
        for i in result:
            print(i)
        ```

- **Searching for a target domain and its subdomains**:
    - *Command line*
        ```bash
        chiasmodon_cli.py --domain example.com --all
        ```
    - *Python*
        ```python
        result = obj.search('example.com',method='domain', all=True)
        
        for i in result:
            print(i)
        ```

- **Searching for a target application ID on the Google Play Store**:
    - *Command line*
        ```bash
        chiasmodon_cli.py --app com.discord
        ```
    - *Python*
        ```python
        result = obj.search('com.discord',method='app')

        for i in result:
            print(i)
        ```

- **Searching for a target ASN**:
    - *Command line*
        ```bash
        chiasmodon_cli.py --asn AS123 --view-type cred
        ```
    - *Python*
        ```python
        result = obj.search('AS123',method='asn', view_type='cred')

        for i in result:
            print(i)
        ```


- **earching for a target username**:
    - *Command line*
        ```bash
        chiasmodon_cli.py --username someone
        ```
    - *Python*
        ```python
        result = obj.search('someone',method='username')

        for i in result:
            print(i)
        ```

- **Searching for a target password**:

    - *Command line*
        ```bash
        chiasmodon_cli.py --password example@123
        ```
    - *Python*
        ```python
        result = obj.search('example@123',method='password')

        for i in result:
            print(i)
        ```

- **Searching for a target CIDR**:

    - *Command line*
        ```bash
        chiasmodon_cli.py --cidr x.x.x.x/24
        ```
    - *Python*
        ```python
        result = obj.search('x.x.x.x/24',method='cidr')

        for i in result:
            print(i)
        ```

- **Searching for target credentials by domain emails**:

    - *Command line*
        ```bash
        chiasmodon_cli.py --domain example.com --domain-emails
        ```
    - *Python*
        ```python
        result = obj.search('example.com',method='domain', only_domain_emails=True)

        for i in result:
            print(i)
        ```

Please note that these examples represent only a fraction of the available options and use cases. Refer to the documentation for more detailed instructions and explore the full range of features provided by Chiasmodon.


## 💬 Contributions and Feedback

Contributions and feedback are welcome! If you encounter any issues or have suggestions for improvements, please submit them to the Chiasmodon GitHub repository. Your input will help us enhance the tool and make it more effective for the OSINT community.

## 📜License

Chiasmodon is released under the [MIT License](https://opensource.org/licenses/MIT). See the [LICENSE](https://github.com/chiasmodon/LICENSE.txt) file for more details.

## ⚠️Disclaimer

Chiasmodon is intended for legal and authorized use only. Users are responsible for ensuring compliance with applicable laws and regulations when using the tool. The developers of Chiasmodon disclaim any responsibility for the misuse or illegal use of the tool.

## 📢Acknowledgments

Chiasmodon is the result of collaborative efforts from a dedicated team of contributors who believe in the power of OSINT. We would like to express our gratitude to the open-source community for their valuable contributions and support.

