# Download geoip location database and convert it to Tor format for Orbot.
# YOUR_LICENSE_KEY must be replaced with your actual licence key from maxmind.

curl "https://download.maxmind.com/app/geoip_download?edition_id=GeoLite2-Country&license_key=YOUR_LICENSE_KEY&suffix=tar.gz" -o GeoLite2-Country.tar.gz

tar -zxf GeoLite2-Country.tar.gz

mv GeoLite2-Country*/GeoLite2-Country.mmdb ./

python3 mmdb-convert.py GeoLite2-Country.mmdb --make-maven-artifacts
