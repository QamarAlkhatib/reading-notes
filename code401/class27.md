# API Deployment

## Configuring Django Settings: Best Practices

### Managing Django Settings: Issues

- Various environments. Local, dev, ci, qa, staging, production, and so on are common environments. Each environment can have its own unique settings (such as ```DEBUG = True```, more verbose logging, additional apps, mocked data, and so on). You'll need a method for storing all of these Django setup configurations.

- Sensitive information. Each Django project has a ```SECRET KEY```variable. There may also be database passwords and tokens for third-party APIs such as Amazon or Twitter. VCS is unable to save this information.

- Members of a team can share settings.
When working with the settings, you'll need a generic method to avoid human error.
A developer may, for example, install a third-party app or API integration but neglect to provide appropriate parameters.
This can be problematic on large (or even mid-sized) projects.

- Django settings are written in Python.
This is both a curse and a blessing in one.
It provides a lot of freedom, but it can also be a problem because, instead of key-value pairs, ```settings.py``` can have some pretty complicated logic.

## Different Approaches to Configuration

Without hardcoding Django settings, there is no built-in global mechanism to configure them. However, literature, open-source software, and work initiatives offer numerous suggestions and techniques on how to do it best. Let's take a look at the most popular ones and see what their flaws and merits are.

-------------

## SSH Tutorial

SSH stands for Secure Shell.
Secure Shell, or SSH, is a remote administration protocol that allows users to administer and modify distant servers via the Internet. The service was designed to be a secure alternative to unencrypted Telnet, and it employs cryptographic techniques to ensure that all communication to and from the remote server is encrypted. It allows you to authenticate a remote user, send inputs from the client to the host, and then relay the output back to the client.

## Understanding the Different Types of Encryption

SSH has a significant advantage over its predecessors in that it uses encryption to ensure secure data transit between the host and the client. The host is the remote server you're trying to connect to, and the client is the machine you're using to connect to it. SSH makes use of three different encryption technologies:

- Symmetrical encryption: Symmetric encryption is a form of encryption where a secret key is used for both encryption and decryption of a message by both the client and the host. Effectively, any one possessing the key can decrypt the message being transferred.

- Asymmetrical encryption: Unlike symmetrical encryption, asymmetrical encryption uses two separate keys for encryption and decryption. These two keys are known as the public key and the private key. Together, both these keys form a public-private key pair.

- Hashing: One-way hashing is another form of cryptography used in Secure Shell Connections. One-way-hash functions differ from the above two forms of encryption in the sense that they are never meant to be decrypted. They generate a unique value of a fixed length for each input that shows no clear trend which can exploited. This makes them practically impossible to reverse.

## Authenticating the User

Authenticating the user's credentials is the final step before the user is permitted access to the server.
Most SSH users use a password for this.
The user is then prompted to provide their login and password.
These credentials are safely transmitted across the symmetrically encrypted tunnel, ensuring that they are not intercepted by a third party.


Despite the fact that passwords are encrypted, they are not recommended for secure connections.
Because many bots may simply brute force simple or default passwords to obtain access to your account, this is the case.
SSH Key Pairs is the suggested choice instead.


These are a collection of asymmetric keys that can be used to authenticate a user without requiring them to enter a password. 