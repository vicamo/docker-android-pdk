FROM vicamo/java:jessie-oracle-java-6-jdk

RUN echo "deb http://http.debian.net/debian wheezy main" > /etc/apt/sources.list.d/http.debian.net_wheezy.list \
	&& dpkg --add-architecture i386 \
	&& apt-get update \
	&& apt-get install --no-install-recommends -y --force-yes \
		bison \
		build-essential \
		ccache \
		file \
		flex \
		g++-multilib \
		git \
		gnupg \
		gperf \
		libgl1-mesa-dev \
		libgl1-mesa-glx:i386 \
		libncurses5-dev:i386 \
		libswitch-perl \
		libx11-dev \
		libx11-dev:i386 \
		libxml2-utils \
		less \
		make=3.81-8.2 \
		python-chardet \
		unzip \
		wget \
		zip \
		zlib1g-dev \
		zlib1g-dev:i386 \
	&& apt-get clean \
	&& rm -f /var/lib/apt/lists/*_dists_* \
	&& ln -s libGL.so.1.2.0 /usr/lib/i386-linux-gnu/libGL.so

RUN wget -nv -O /usr/bin/repo https://storage.googleapis.com/git-repo-downloads/repo \
	&& chmod a+x /usr/bin/repo

ENV USE_CCACHE 1
