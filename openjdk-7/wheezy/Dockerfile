FROM vicamo/openjdk:wheezy-7-jdk

RUN dpkg --add-architecture i386 \
	&& apt-get update \
	&& apt-get install --no-install-recommends -y \
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
		libgl1-mesa-dri \
		libgl1-mesa-dri:i386 \
		libgl1-mesa-glx:i386 \
		libncurses5-dev:i386 \
		libswitch-perl \
		libx11-dev \
		libx11-dev:i386 \
		libxml2-utils \
		less \
		make \
		python-chardet \
		telnet \
		unzip \
		wget \
		zip \
		zlib1g-dev \
		zlib1g-dev:i386 \
	&& apt-get clean \
	&& ln -s libGL.so.1.2.0 /usr/lib/i386-linux-gnu/libGL.so \
	&& rm -f /var/lib/apt/lists/*_dists_*

RUN wget -nv -O /usr/bin/repo https://storage.googleapis.com/git-repo-downloads/repo \
	&& chmod a+x /usr/bin/repo

ENV USE_CCACHE 1
