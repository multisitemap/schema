# schema.multisitemap.com

+ domain-dns
+ domain-nameserwers
+ ip-server
+ domain-provider.domain-name.nameserwer.server_provider.server_ip

## Manualnie
Mapa może być tworzona odręcznie w celu weryfikacji poprz inframonit.com który używa narzędzia infrash.com do sprawdzenia statusu infrastruktury

## Automatycznie
Mapa może być generowana poprzez skrypty infrash.com
wystarczy podać Endpoint oraz oczekiwane objekty a rezutltaty zostaną wyggenerowane

## Automatyczne generowanie na podstawie pliku CSV

### IN

```csv
domain,https_status,screenshot_png
example1.com
example2.com
example3.com
```

### OUT

```csv
domain,nameservers
example1.com,ns1.com,ns2.com,ns3.com
example2.com,ns1.com,ns2.com,ns3.com
example3.com,ns1.com,ns2.com,ns3.com
```



## Struktura

multisitemap.com

+ inframonit - monitrowanie infrastruktury za pomocą skryptów i usług SaaS
+ infrash - uruchamianie skryptów

## Examples

### domain-nameserwers

```csv
domain,nameservers
example.com,ns1.com,ns2.com,ns3.com
```
