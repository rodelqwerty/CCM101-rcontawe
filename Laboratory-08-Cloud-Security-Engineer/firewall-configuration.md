# Firewall Configuration

## 1. Allow SSH Access

Command:

```bash
sudo ufw allow ssh
```

This rule allows SSH traffic so administrators can remotely manage the server.

## 2. Configure the Default Policies

Commands:

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

The first command blocks incoming connections by default unless an explicit rule allows them. The second command permits outgoing connections by default.

## 3. Activate the Firewall

Command:

```bash
sudo ufw enable
```

Verify the configuration with:

```bash
sudo ufw status verbose
```

## 4. Allow the Web Application

Command:

```bash
sudo ufw allow 8080/tcp
```

Verify the rules with:

```bash
sudo ufw status numbered
```

This rule permits incoming TCP connections on port 8080 for the web application.

## 5. Why SSH Must Be Allowed First

If UFW is enabled before SSH is explicitly allowed, incoming SSH connections may be blocked by the default deny policy, potentially locking remote administrators out of the server.

## 6. Security Summary

The firewall uses a default-deny incoming policy and allows the specific services required for administration and web application access. The configuration should be reviewed regularly to remove unnecessary rules and keep the server's attack surface as small as possible.
