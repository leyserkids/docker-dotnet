FROM mcr.microsoft.com/dotnet/aspnet:6.0-alpine3.14
# Calendar information is provided by International
# Components for Unicode (ICU) for .NET Core on Linux
# To using JapaneseCalendar, ICU should be installed.
RUN apk add --no-cache icu-libs --repository=http://dl-cdn.alpinelinux.org/alpine/edge/main
# https://github.com/dotnet/dotnet-docker/pull/1312
RUN apk add --no-cache tzdata --repository=http://dl-cdn.alpinelinux.org/alpine/edge/main
# Disable the invariant mode
ENV DOTNET_SYSTEM_GLOBALIZATION_INVARIANT=false \
    LC_ALL=en_US.UTF-8 \
    LANG=en_US.UTF-8 \
    TZ=Etc/UTC