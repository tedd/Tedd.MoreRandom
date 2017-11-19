# Tedd.MoreRandom
Drop in replacement for System.Random based on RNGCryptoServiceProvider.

## Background
System.Random is based on so called "pseudorandom" algorithm. This means that given a seed (default this is number of milliseconds since computer was started) math is used to generate seemingly random numbers. Given the same seed, a sequence of random numbers will look the same every time. For most cases this is fine, but in some cases you need more random data. One such case is cryptography, where a pseudorandom generator such as System.Random would generate a predictable sequence of numbers.

System.Security.Cryptography.RNGCryptoServiceProvider provides "cryptography grade random" numbers. These numbers are a bit more random as they are provided by the operating system, which has methods of collecting random data.

## Compatibility
Created using .Net Standard 2.0.

## Unit testing
xUnit in .Net Core with near 100% code coverage. Boundary checks as well as average check on vast number of samples.

## Links
https://msdn.microsoft.com/en-us/library/system.security.cryptography.rngcryptoserviceprovider(v=vs.110).aspx