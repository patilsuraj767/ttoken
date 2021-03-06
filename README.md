# Ttoken

Ttoken is a command-line program to generate time-based token/OTP.

Apart from generating time-based OTP, it provides the feature of creating pin+token and copies it to the clipboard so that user can enter it anywhere by just the click of Ctrl+v.  

## Installation

```ruby
# yum install epel-release

# yum install ruby rubygems xclip

# gem install ttoken
```

## Usage

Gem provides the executable command-line program - ttoken. 

1) Create the file `/etc/ttoken/ttoken.yml` and enter the below content. 

```ruby
# Issuer - The site or app you are creating the OTP
:issuer: 'Red Hat'

# Time-based token provided by issuer
:token: "1234abcdxyz"

# Enable pin+token
:pinplustoken: yes

```
Make sure you change the issuer and token. 

2) To encrypt and save your password/pin in ttoken use the below command. 

```ruby
# ttoken --encrypt
```

3) Running the ttoken command generates pin+token and will copy it to the clipboard. 


```ruby
# ttoken
```

## Screen

Demo - Connecting to VPN using pin+token.

![Alt text](images/ttoken.gif)

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/patilsuraj767/ttoken.

