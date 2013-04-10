for x in $(grep -l -R 3.0.0-BETA2-SNAPSHOT *); do sed -i -e 's/3.0.0-BETA2-SNAPSHOT/3.0.0.vivo_2/g' $x; done;
