
Sign a nanopub template ( nanopub-template.trig) in the current folder using nanopub-java image from DockerHub:
docker run -it --rm -v ~/.nanopub:/root/.nanopub -v $(pwd):/data umids/nanopub-java sign /data/nanopub.trig

Publish the signed nanopub template
 docker run -it --rm -v ~/.nanopub:/root/.nanopub -v $(pwd):/data umids/nanopub-java publish /data/signed.nanopub.trig


Download the latest release of the Nanobench jar file for the Translator ecosystem by running this command:

curl -s https://api.github.com/repos/vemonet/nanobench/releases/latest | grep "browser_download_url.*.jar" | cut -d : -f 2,3 | tr -d \" | wget -O ./nanobench.jar -i -

