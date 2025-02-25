# Dnsrecon
`dnsrecon` is a powerful tool for DNS enumeration and reconnaissance in penetration testing. It can be used to gather detailed information about a domain. Below are some common `dnsrecon` commands and examples you can use in Kali Linux:

### Basic Commands

1. **Basic DNS Enumeration**
   ```bash
   dnsrecon -d example.com
   ```
   This command performs a basic DNS enumeration for the domain `example.com`.

2. **Zone Transfer**
   ```bash
   dnsrecon -d example.com -t axfr
   ```
   Attempts a zone transfer (AXFR) to retrieve the entire DNS zone if the DNS server allows it.

3. **Brute Force Subdomain Enumeration**
   ```bash
   dnsrecon -d example.com -t brt -f subdomains.txt
   ```
   This command uses a wordlist (`subdomains.txt`) to brute force subdomains of `example.com`.

4. **Reverse Lookup**
   ```bash
   dnsrecon -r 192.0.2.0/24
   ```
   Performs a reverse DNS lookup for the specified IP range.

5. **DNS Walk**
   ```bash
   dnsrecon -d example.com -t walk
   ```
   This command performs a DNS walk to discover all the DNS records.

### Advanced Usage

6. **Enumerate All Records**
   ```bash
   dnsrecon -d example.com -t std
   ```
   Enumerates all DNS records (A, AAAA, MX, TXT, etc.) for the specified domain.

7. **Search for Specific Record Types**
   ```bash
   dnsrecon -d example.com -t mx
   ```
   This command specifically looks for MX records for `example.com`.

8. **Output Results to File**
   ```bash
   dnsrecon -d example.com -a -o output.txt
   ```
   This command saves all enumeration results to `output.txt`.

9. **Use a Specific DNS Server**
   ```bash
   dnsrecon -d example.com -n 8.8.8.8
   ```
   Specifies a DNS server (in this case, Google’s DNS) to use for the queries.

### Example of a Full Command
Here’s an example that combines several options:
```bash
dnsrecon -d example.com -t brt -f subdomains.txt -n 8.8.8.8 -a -o results.txt
```
This command will:
- Perform a brute force subdomain scan using a specified file.
- Use Google’s DNS server.
- Include all available record types.
- Output the results to `results.txt`.

### Conclusion
`dnsrecon` is a versatile tool, and these commands can help you gather valuable information during a penetration test or security assessment. Make sure to have permission to test the domains you are querying!




                                                      ALTERNATIVE
Here are some common `dnsrecon` commands and examples on Kali Linux:

1. **Perform Brute Force Subdomain Enumeration**:
   ```
   dnsrecon -d example.com -t brt
   ```
   This command will perform a brute-force attack to discover subdomains of the target domain `example.com`.

2. **Perform Zone Transfer**:
   ```
   dnsrecon -d example.com -t axfr
   ```
   This command will attempt to perform a zone transfer for the target domain `example.com`.

3. **Perform DNS Cache Snooping**:
   ```
   dnsrecon -d example.com -t snoop -n 8.8.8.8
   ```
   This command will perform DNS cache snooping using the Google DNS server `8.8.8.8` to discover potentially sensitive information about the target domain `example.com`.

4. **Perform Reverse DNS Lookup**:
   ```
   dnsrecon -r 192.168.1.0/24 -n 8.8.8.8
   ```
   This command will perform a reverse DNS lookup for the IP range `192.168.1.0/24` using the Google DNS server `8.8.8.8`.

5. **Perform DNS Wildcard and CNAME detection**:
   ```
   dnsrecon -d example.com -t std
   ```
   This command will perform standard DNS enumeration to detect any wildcard and CNAME records for the target domain `example.com`.

6. **Perform DNS Txt, MX, and NS record enumeration**:
   ```
   dnsrecon -d example.com -t rvl
   ```
   This command will perform a thorough enumeration of the TXT, MX, and NS records for the target domain `example.com`.

7. **Perform DNS Dictionary Attack**:
   ```
   dnsrecon -d example.com -D /path/to/wordlist.txt -t brt
   ```
   This command will perform a dictionary-based attack to discover subdomains of the target domain `example.com` using the provided wordlist at `/path/to/wordlist.txt`.

These are just a few examples of the many options and capabilities of the `dnsrecon` tool. You can refer to the tool's man page or documentation for more information on additional features and usage.





                                                              ALTERNATIVE
Here are some common `dnsrecon` commands and examples on Kali Linux:

1. **Perform Brute Force Subdomain Enumeration**:
   ```
   dnsrecon -d example.com -t brt
   ```
   This command will perform a brute-force attack to discover subdomains of the target domain `example.com`.

2. **Perform Zone Transfer**:
   ```
   dnsrecon -d example.com -t axfr
   ```
   This command will attempt to perform a zone transfer for the target domain `example.com`.

3. **Perform DNS Cache Snooping**:
   ```
   dnsrecon -d example.com -t snoop -n 8.8.8.8
   ```
   This command will perform DNS cache snooping using the Google DNS server `8.8.8.8` to discover potentially sensitive information about the target domain `example.com`.

4. **Perform Reverse DNS Lookup**:
   ```
   dnsrecon -r 192.168.1.0/24 -n 8.8.8.8
   ```
   This command will perform a reverse DNS lookup for the IP range `192.168.1.0/24` using the Google DNS server `8.8.8.8`.

5. **Perform DNS Wildcard and CNAME detection**:
   ```
   dnsrecon -d example.com -t std
   ```
   This command will perform standard DNS enumeration to detect any wildcard and CNAME records for the target domain `example.com`.

6. **Perform DNS Txt, MX, and NS record enumeration**:
   ```
   dnsrecon -d example.com -t rvl
   ```
   This command will perform a thorough enumeration of the TXT, MX, and NS records for the target domain `example.com`.

7. **Perform DNS Dictionary Attack**:
   ```
   dnsrecon -d example.com -D /path/to/wordlist.txt -t brt
   ```
   This command will perform a dictionary-based attack to discover subdomains of the target domain `example.com` using the provided wordlist at `/path/to/wordlist.txt`.

These are just a few examples of the many options and capabilities of the `dnsrecon` tool. You can refer to the tool's man page or documentation for more information on additional features and usage.




`dnsrecon` is a powerful DNS reconnaissance tool that can be used to gather information about a domain's DNS records, including IP addresses, mail servers, name servers, and more. Here are some common `dnsrecon` commands and examples on Kali Linux:

**Basic Commands**

1. `dnsrecon -h`: Displays the help menu and available options.
2. `dnsrecon -d <domain>`: Performs a standard DNS reconnaissance scan on the specified domain.

**Example:** `dnsrecon -d example.com`

**Scanning for DNS Records**

1. `dnsrecon -a <domain>`: Scans for all DNS records (A, NS, MX, SOA, TXT, etc.) for the specified domain.

**Example:** `dnsrecon -a example.com`

2. `dnsrecon -t <record_type> <domain>`: Scans for a specific DNS record type (e.g., A, MX, NS) for the specified domain.

**Example:** `dnsrecon -t MX example.com` (scans for MX records)

**Scanning for Subdomains**

1. `dnsrecon -s <domain>`: Scans for subdomains of the specified domain.

**Example:** `dnsrecon -s example.com`

2. `dnsrecon -s -d <domain>`: Scans for subdomains and performs a DNS reconnaissance scan on each subdomain.

**Example:** `dnsrecon -s -d example.com`

**Scanning for DNS Servers**

1. `dnsrecon -n <domain>`: Scans for DNS servers (name servers) for the specified domain.

**Example:** `dnsrecon -n example.com`

**Scanning for Mail Servers**

1. `dnsrecon -m <domain>`: Scans for mail servers (MX records) for the specified domain.

**Example:** `dnsrecon -m example.com`

**Advanced Options**

1. `dnsrecon -c <config_file>`: Uses a custom configuration file for the scan.

**Example:** `dnsrecon -c myconfig.txt -d example.com`

2. `dnsrecon -o <output_file>`: Saves the scan results to a file.

**Example:** `dnsrecon -o output.txt -d example.com`

3. `dnsrecon -v`: Enables verbose mode, which provides more detailed output.

**Example:** `dnsrecon -v -d example.com`

Remember to use `dnsrecon` responsibly and only scan domains that you have permission to scan.






                                            ALTERNATIVE
`dnsrecon` is a powerful tool for DNS enumeration and reconnaissance in Kali Linux. Below are some common commands and examples to help you get started.

### Basic Commands

1. **Basic DNS Enumeration**
   ```bash
   dnsrecon -d example.com
   ```
   This command performs basic DNS enumeration on `example.com`.

2. **Reverse Lookup**
   ```bash
   dnsrecon -r 192.168.1.0/24
   ```
   This command performs a reverse lookup on the IP range `192.168.1.0/24`.

3. **Zone Transfer**
   ```bash
   dnsrecon -d example.com -t axfr
   ```
   Attempts a zone transfer for `example.com`. This is useful if the DNS server is misconfigured.

4. **Brute Force Subdomain Enumeration**
   ```bash
   dnsrecon -d example.com -D subdomains.txt -t brt
   ```
   This command uses a wordlist (`subdomains.txt`) to brute-force subdomains for `example.com`.

5. **DNS Record Types**
   ```bash
   dnsrecon -d example.com -t any
   ```
   This retrieves all available DNS records for `example.com`.

### Advanced Commands

1. **Performing All DNS Queries**
   ```bash
   dnsrecon -d example.com -t std
   ```
   This command performs standard DNS queries to gather information like A, AAAA, MX, NS, etc.

2. **Using a Custom DNS Server**
   ```bash
   dnsrecon -d example.com -s 8.8.8.8
   ```
   This runs the enumeration using Google’s public DNS server.

3. **Output to File**
   ```bash
   dnsrecon -d example.com -o output.txt
   ```
   This saves the results of the DNS enumeration to `output.txt`.

4. **JSON Output**
   ```bash
   dnsrecon -d example.com -j output.json
   ```
   This command outputs results in JSON format.

5. **Specifying DNS Record Types**
   ```bash
   dnsrecon -d example.com -t brt -D subdomains.txt -j output.json
   ```
   This combines brute force subdomain enumeration and outputs the results in JSON.

### Conclusion

These commands provide a solid foundation for using `dnsrecon` in Kali Linux for DNS reconnaissance. Always ensure you have permission to perform these activities on any domain to avoid legal issues.






                                                                 ALTERNATIVE
DNSRecon is a powerful DNS enumeration tool in Kali Linux used for reconnaissance on domains. It can discover subdomains, retrieve DNS records, and perform zone transfers.

Here's how to use DNSRecon with examples:

**1. Installation (if not already installed):**

```bash
sudo apt install dnsrecon
```

**2. Basic Usage:**

*   **To enumerate DNS records for a domain:**

    ```bash
    dnsrecon -d <domain>
    ```

    *   Replace `<domain>` with the target domain name (e.g., `example.com`).
    *   This will perform a standard enumeration, including SOA, NS, A, AAAA, MX, and SRV records.
*   **Using a specific name server:**

    ```bash
    dnsrecon -d <domain> -n <nameserver>
    ```

    *   Replace `<nameserver>` with the DNS server to use. If none is given, the SOA of the target will be used. Multiple servers can be specified using a comma separated list.

**3. Enumeration Types (`-t` option):**

*   **Specify the type of enumeration:**

    ```bash
    dnsrecon -d <domain> -t <type>
    ```

    *   Replace `<type>` with one of the following:
        *   `std`:  SOA, NS, A, AAAA, MX, and SRV records (standard enumeration).
        *   `rvl`: Reverse lookup of a given CIDR or IP range.
        *   `brt`: Brute force domains and hosts using a given dictionary.
        *   `srv`: SRV records.
        *   `axfr`: Test all NS servers for a zone transfer.
        *   `bing`: Perform Bing search for subdomains and hosts.
        *   `yand`: Perform Yandex search for subdomains and hosts.

**4. Brute Force Subdomains:**

*   **Using a dictionary file:**

    ```bash
    dnsrecon -d <domain> -D <dictionary_file> -t brt
    ```

    *   Replace `<dictionary_file>` with the path to a wordlist (e.g., `/usr/share/wordlists/dnsmap.txt`).

**5. Zone Transfer:**

*   **Attempt a zone transfer:**

    ```bash
    dnsrecon -d <domain> -t axfr
    ```

    *   This attempts to retrieve a complete list of DNS records from the target's name servers.
    *   To perform a zone transfer along with standard enumeration:
        ```bash
        dnsrecon -d <domain> -a
        ```

**6. Reverse DNS Lookup:**

*   **Perform a reverse lookup of an IP range:**

    ```bash
    dnsrecon -r <IP_range>
    ```

    *   Replace `<IP_range>` with the IP range in the format `first-last` or `range/bitmask` (e.g., `192.168.1.1-192.168.1.254` or `192.168.1.0/24`).

**7. Output Options:**

*   **Save output to a file:**

    *   XML: `dnsrecon -d <domain> --xml <output_file.xml>`
    *   CSV: `dnsrecon -d <domain> --csv <output_file.csv>`
    *   JSON: `dnsrecon -d <domain> --json <output_file.json>`

**8. Other useful options:**

*   `-w`: Perform deep whois record analysis and reverse lookup of IP ranges found during standard enumeration.
*   `-s`: Perform a reverse lookup of IPv4 ranges in the SPF record with standard enumeration.
*   `-k`: Perform crt.sh enumeration with standard enumeration.
*   `--threads <number>`:  Specify the number of threads to use (default is 20).
*   `--tcp`: Use TCP protocol for queries.

**Important Notes:**

*   Always use DNSRecon ethically and responsibly, and only on systems you have permission to test.
*   DNSRecon is pre-installed on Kali Linux.
*   Keep Kali Linux updated to have the latest version of DNSRecon.


---
![server_inject_icon](https://pfst.cf2.poecdn.net/base/image/0e8698a6e80a985ec6d5f4d175c17866cee4b502ac78ccea3d02bb90fdca0b9f?w=100&h=33)
Related searches:
+ [dnsrecon commands examples kali](https://www.google.com/search?q=dnsrecon+commands+examples+kali&client=app-vertex-grounding-quora-poe)
+ [dnsrecon usage examples](https://www.google.com/search?q=dnsrecon+usage+examples&client=app-vertex-grounding-quora-poe)






                                                      ALTERNATIVE
  DNSRecon is a powerful command-line tool used for DNS reconnaissance and enumeration, particularly useful for security professionals and ethical hackers. It allows users to gather information about a target domain, including subdomains, DNS records, and more. Below are some common commands and examples of how to use DNSRecon on Kali Linux.

### Basic Command Structure
The basic syntax for using DNSRecon is:
```
dnsrecon <options> <target>
```

### Common Commands and Options
- **General Enumeration**: To perform a standard enumeration of a domain, use:
  ```
  dnsrecon -d example.com
  ```
  This command retrieves various DNS records such as SOA, NS, A, AAAA, MX, and SRV records.

- **Brute Force Subdomains**: To brute-force subdomains using a dictionary file, use:
  ```
  dnsrecon -d example.com -D /usr/share/wordlists/dnsmap.txt -t brt
  ```
  This command attempts to find subdomains listed in the specified dictionary.

- **Zone Transfer**: To check for zone transfers, which can reveal all DNS records, use:
  ```
  dnsrecon -d example.com -a
  ```
  This command attempts an AXFR (zone transfer) request against all name servers.

- **Reverse Lookup**: To perform a reverse lookup on a given IP range, use:
  ```
  dnsrecon -r 192.168.1.0/24 -t rvl
  ```
  This command retrieves hostnames associated with the specified IP range.

- **Save Output**: To save the output to an XML file, you can use:
  ```
  dnsrecon -d example.com --xml dnsrecon.xml
  ```
  This command saves the results of the enumeration in XML format.

### Example Usage
1. **Enumerating Subdomains**:
   ```
   dnsrecon -d microsoft.com
   ```
   This command will perform a general enumeration against the domain `microsoft.com` and display various DNS records found.

2. **Retrieving DNS Records**:
   ```
   dnsrecon -d google.com -t std
   ```
   This command retrieves standard DNS records for `google.com`, including SOA and NS records.

3. **Brute Force with Dictionary**:
   ```
   dnsrecon -d example.com -D /usr/share/wordlists/dnsmap.txt -t brt
   ```
   This command attempts to discover subdomains of `example.com` using a specified wordlist.

### Installation
DNSRecon is typically pre-installed on Kali Linux. If it's not available, you can install it using:
```
sudo apt install dnsrecon
```

### Conclusion
DNSRecon is a versatile tool for DNS enumeration and reconnaissance, providing various options to gather detailed information about target domains. By using the commands outlined above, users can effectively assess the security posture of a network.

---
Learn more:
1. [dnsrecon | Kali Linux Tools](https://www.kali.org/tools/dnsrecon/)
2. [What is dnsrecon Full Guide. DNS reconnaissance is an important part… | by TechMindXperts | Medium](https://medium.com/@techmindxperts/what-is-dnsrecon-full-guide-with-examples-355aba308332)
3. [DNSRecon - A powerful DNS enumeration script - GeeksforGeeks](https://www.geeksforgeeks.org/dnsrecon-a-powerful-dns-enumeration-script/)
