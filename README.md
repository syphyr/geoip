# geoip

curl "https://download.maxmind.com/app/geoip_download?edition_id=GeoLite2-Country&license_key=YOUR_LICENSE_KEY&suffix=tar.gz" -o GeoLite2-Country.tar.gz

tar -zxf GeoLite2-Country.tar.gz

mv GeoLite2-Country*/GeoLite2-Country.mmdb ./
