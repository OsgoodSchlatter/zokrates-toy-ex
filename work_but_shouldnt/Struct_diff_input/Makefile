proof:
	zokrates compile --debug -i bob/add.zok -o bob/add
	zokrates compute-witness --verbose -i bob/add -a 0
	zokrates setup -i bob/add
	cp proving.key alice
	zokrates compile --debug -i alice/add.zok -o alice/add
	zokrates compute-witness --verbose -i alice/add -a 1
	zokrates generate-proof -i alice/add
	cp proof.json bob
	cd bob
	zokrates verify


clean: 
	rm -rf alice/*.json alice/out* alice/*.key alice/witness alice/get_hash	alice/add
	rm -rf bob/*.key bob/*.json bob/out.* bob/add bob/get_hash bob/witness
	rm -rf *.key
