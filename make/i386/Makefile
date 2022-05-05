all:
	sudo mkdir -p /home/cogroid/local/libatomic_ops/i386
	cp -f ./atomic_ops.h ../../src/
	cd ../../; \
	./configure \
	ABI=32 \
	--build=i386-linux-gnu \
	--host=i386-linux-gnu \
	CXXFLAGS="-v -m32 -march=i386 " \
	CPPFLAGS="-v -m32 -march=i386 " \
	CFLAGS="-v -m32 -march=i386 " \
	LDFLAGS="-v -m32 -march=i386 " \
	--prefix=/home/cogroid/local/libatomic_ops/i386; \
	make

install:
	sudo sh -c 'cd ../../; \
	export CPPFLAGS="-v -m32 -march=i386 "; \
	export CXXFLAGS="-v -m32 -march=i386 "; \
	export CFLAGS="-v -m32 -march=i386 "; \
	export LDFLAGS="-v -m32 -march=i386 "; \
	make install;'

clean:
	cd ../../; \
	make clean