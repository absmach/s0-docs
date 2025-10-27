# Connecting S0 to SuperMQ

After cloning the SuperMQ repository, follow these steps using the CLI.

## Create user

```bash
./build/cli users create <firstname> <lastname> <email> <username> <password>
```

## Create a User Token

```bash
./build/cli users token <username> <password>
```

This yields the `ACCESSTOKEN` and `REFRFESHTOKEN`
Copy the `ACCESSTOKEN` and save it as environment variable.

```bash
export ACCESSTOKEN=<your access token>
```

To access your environment variables, use the dollar operator.

```bash
echo $ACCESSTOKEN
```

## Create a Domain

```bash
./build/cli doamins <domain name> create <route> $ACCESSTOKEN
```

This yields the Domain ID, which you store as an environment variable

## Create a Channel

```bash
./build/cli channels '{"name":"<channel_name>"}' create $DOMAINID $ACCESSTOKEN
```

This yields the Channel ID, which you store as an environment variable

## Create a Client

```bash
./build/cli clients '{"name":"<client_name>"}' create $DOMAINID $ACCESSTOKEN
```

This yield the `CLIENTID` and `CLIENTSECRET` which you store as environment variableS

---
