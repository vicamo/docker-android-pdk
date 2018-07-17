FROM vicamo/openjdk:cosmic-8-jdk

RUN dpkg --add-architecture i386 \
	&& apt-get update \
	&& apt-get install --no-install-recommends -y \
		adb \
		android-tools-fsutils \
		bison \
		build-essential \
		ccache \
		curl \
		fastboot \
		file \
		flex \
		g++-multilib \
		git \
		gnupg \
		gperf \
		less \
		libgl1 \
		libgl1:i386 \
		libxml2-utils \
		make \
		telnet \
		unzip \
		wget \
		zip \
	&& apt-get install --no-install-recommends -y \
		locales \
		lsb-release \
		pbzip2 \
	&& sed 's,^# fr_FR.UTF-8 UTF-8,fr_FR.UTF-8 UTF-8,' -i /etc/locale.gen \
	&& locale-gen \
	&& apt-get clean \
	&& rm -f /var/lib/apt/lists/*_dists_*

RUN wget -nv -O /usr/bin/repo https://storage.googleapis.com/git-repo-downloads/repo \
	&& chmod a+x /usr/bin/repo

ENV USE_CCACHE 1
