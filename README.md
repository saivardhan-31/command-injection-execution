# command-injection-execution
This project demonstrates command injection attacks using DVWA and bWAPP, including basic, blind, and filter bypass techniques, to understand how improper input validation leads to server command execution vulnerabilities.

## Objective
The main objective is to learn how attackers execute system commands on a server through improper input validation and understand the impact of command injection vulnerabilities in real-world applications.

## Lab Environment
- Kali Linux
- DVWA (Damn Vulnerable Web Application)
- bWAPP (Buggy Web Application)
- Burp Suite
- Netcat (nc)

## Tasks Performed
### Part 1: DVWA – Command Injection
- Tested command injection on Low and High security levels
- Executed basic payloads (whoami, id, ls)
- Performed blind command injection using ping and delay-based payloads
- Intercepted and modified requests using Burp Suite

### Part 2: bWAPP – OS Command Injection
- Performed basic command injection using separators (;, &&, |, &)
- Tested filter bypass using URL encoding and alternative payloads
- Conducted blind command injection using sleep and ping delays
- Attempted reverse shell using Netcat and Bash payloads

## Payload Examples
- `127.0.0.1; whoami`
- `127.0.0.1 && id`
- `127.0.0.1 | ls`
- `127.0.0.1 && sleep 5`
- `127.0.0.1%26%26cat%20/etc/passwd`

## Tools Used
- nmap (network scanning)
- Burp Suite (request interception)
- Netcat (reverse shell listener)
- Browser Developer Tools

## Key Learning Outcomes
- Understanding command injection vulnerability
- Difference between basic and blind command injection
- Filter bypass techniques
- Importance of input validation and secure coding practices

## Ethical Note
All tests were performed in a legal lab setup (DVWA and bWAPP) for educational and ethical hacking purposes only. No real systems were targeted.

## Conclusion
This project provided hands-on experience in identifying and exploiting command injection vulnerabilities, highlighting the risks of improper input sanitization and the importance of secure server-side validation.

