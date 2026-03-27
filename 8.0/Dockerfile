FROM mcr.microsoft.com/dotnet/aspnet:8.0.25-alpine3.23-amd64
# Calendar information is provided by International
# Components for Unicode (ICU) for .NET Core on Linux
# To using JapaneseCalendar, ICU should be installed.
RUN apk add --no-cache icu-libs icu-data-full tzdata
# Disable the invariant mode
# Set default port: https://learn.microsoft.com/en-us/dotnet/core/compatibility/containers/8.0/aspnet-port
ENV DOTNET_SYSTEM_GLOBALIZATION_INVARIANT=false \
    ASPNETCORE_HTTP_PORTS=80 \
    LC_ALL=en_US.UTF-8 \
    LANG=en_US.UTF-8 \
    TZ=Etc/UTC
