FROM mcr.microsoft.com/dotnet/core/aspnet:3.0.0-preview7-alpine3.9
# Calendar information is provided by International
# Components for Unicode (ICU) for .NET Core on Linux
# To using JapaneseCalendar, ICU should be installed.
RUN apk add --no-cache icu-libs --repository=http://dl-cdn.alpinelinux.org/alpine/edge/main
# Disable the invariant mode
ENV DOTNET_SYSTEM_GLOBALIZATION_INVARIANT=false \
    LC_ALL=en_US.UTF-8 \
    LANG=en_US.UTF-8 \
    TZ=Etc/UTC