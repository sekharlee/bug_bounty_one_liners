# subdomains Finder from Rapid dns 

  curl -s "https://rapiddns.io/subdomain/domain.com?full=1#result" | grep "<td>" |grep -v href|grep tesla.com|sed 's/<td>//g'|sed 's\</td>\\g'
