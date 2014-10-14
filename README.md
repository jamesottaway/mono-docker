# Supported tags and respective `Dockerfile` links

- [`latest` (Dockerfile)] [dockerfile-latest]
- [`3.6.0` (Dockerfile)] [dockerfile-3.6.0]

# What is Mono?

Mono, the open source development platform based on the .NET framework, allows developers to build cross-platform applications with improved developer productivity. Mono’s .NET implementation is based on the ECMA standards for C# and the Common Language Infrastructure.

Sponsored previously by Novell and now by Xamarin, the Mono project has an active and enthusiastic contributing community. Mono includes both developer tools and the infrastructure needed to run .NET client and server applications.

> [mono-project.com/docs/about-mono] [mono-about]

![](logo.png)

# How to use this image

## Compile your app inside the Docker container

There may be occasions where it is not appropriate to run your app inside a container. To compile, but not run your app inside the Docker instance, you can write something like:

```
docker run --rm -v "$(pwd)":/usr/src/myapp -w /usr/src/myapp jamesottaway/mono:latest xbuild /t:build
```

This will add your current directory as a volume to the container, set the working directory to the volume, and run the command `xbuild /t:clean` which will tell Mono to compile the project in the working directory and output the executable to `myapp`.

# License

View [license information][mono-license] for the software contained this image.

# User Feedback

## Issues

If you have any problems with or questions about this image, please contact us through a [GitHub issue][github-mono-docker-issues].

You can also reach many of the official image maintainers via the `#docker-library` IRC channel on [Freenode][freenode].

## Contributing

You are invited to contribute new features, fixes, or updates, large or small; we are always thrilled to receive pull requests, and do our best to process them as fast as we can.

Before you start to code, we recommend discussing your plans through a [GitHub issue][github-mono-docker-issues], especially for more ambitious contributions. This gives other contributors a chance to point you in the right direction, give you feedback on your design, and help you find out if someone else is working on the same thing.

[dockerfile-latest]: https://github.com/jamesottaway/mono-docker/blob/master/Dockerfile
[dockerfile-3.6.0]: https://github.com/jamesottaway/mono-docker/blob/3.6.0/Dockerfile
[mono-about]: http://www.mono-project.com/docs/about-mono/
[mono-license]: http://www.mono-project.com/docs/faq/licensing/
[github-mono-docker-issues]: https://github.com/jamesottaway/mono-docker/issues
[freenode]: https://freenode.net/
