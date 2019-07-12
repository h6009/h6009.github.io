```markdown
iptables -t nat -A PREROUTING -p tcp --dport 10622 -j DNAT --to 10.10.10.106:22
```