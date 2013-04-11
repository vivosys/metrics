for x in $(grep -l -R 3.0.0-BETA2-SNAPSHOT *); do sed -i -e 's/3.0.0-BETA2-SNAPSHOT/3.0.0.vivo_2/g' $x; done;

REPO_ID=vivosys-repo
REPO_URL=https://tools.vivosys.com/artifactory/ext-release-local
mvn \
  -Dgpg.skip \
  -DaltDeploymentRepository=$REPO_ID::default::$REPO_URL \
  source:jar javadoc:jar deploy
