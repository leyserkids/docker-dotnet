FROM mcr.microsoft.com/dotnet/aspnet:8.0.13-alpine3.21-amd64
# Calendar information is provided by International
# Components for Unicode (ICU) for .NET Core on Linux
# To using JapaneseCalendar, ICU should be installed.
RUN apk add --no-cache icu-libs --repository=http://dl-cdn.alpinelinux.org/alpine/edge/main
RUN apk add --no-cache icu-data-full --repository=http://dl-cdn.alpinelinux.org/alpine/edge/main
# https://github.com/dotnet/dotnet-docker/pull/1312
RUN apk add --no-cache tzdata --repository=http://dl-cdn.alpinelinux.org/alpine/edge/main
# Disable the invariant mode
# Set default port: https://learn.microsoft.com/en-us/dotnet/core/compatibility/containers/8.0/aspnet-port
ENV DOTNET_SYSTEM_GLOBALIZATION_INVARIANT=false \
    ASPNETCORE_HTTP_PORTS=80 \
    LC_ALL=en_US.UTF-8 \
    LANG=en_US.UTF-8 \
    TZ=Etc/UTC