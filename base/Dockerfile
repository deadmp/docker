FROM elixir

LABEL Alexander Troshin <mail@novium.pw>

RUN mix local.hex --force

RUN apt-get update
RUN curl -sL https://deb.nodesource.com/setup_8.x | apt-get install -y inotify-tools nodejs
RUN mix archive.install --force https://github.com/phoenixframework/archives/raw/master/phoenix_new.ez

RUN mix local.rebar --force

WORKDIR /usr/share/code