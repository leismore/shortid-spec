# Leismore ShortID Specification v3.0.0 LTS




------------------------------------------------------------------------------

27 February 2023

## Authors

* Kyle Chine [Leismore](https://www.leismore.co) <https://kylechine.leismore.co>

## Copyright

[GNU Free Documentation License Version 1.3](https://lmos.leismore.org/shortid-spec/v3-0-0/rep/LICENSE)

## Canonical URLs

* This version: <https://lmos.leismore.org/shortid-spec/v3-0-0/rep/README.md>
* Latest version: <https://lmos.leismore.org/shortid-spec/latest/rep/README.md>

* Project Homepage: <https://lmos.leismore.org/shortid-spec>
* GitHub: <https://github.com/leismore/shortid-spec>

------------------------------------------------------------------------------




## Introduction

Leismore ShortID is a universally unique identifier based on [Nano ID](https://github.com/ai/nanoid) (Sitnik [2017] 2021). This document describes its purpose, format, recommended comparison method, and other technical details.

## Purpose and Designing Considerations

Ideally, a universally unique identifier exposing to end-users or external applications via digital medias, should be:

1. No collision in the near future
2. Friendly for human readers
3. URL friendly character set
4. Short and fixed length

## Format

* Character set ( `nolookalikes` from [Nanoid-Dictionary](https://github.com/CyberAP/nanoid-dictionary) (Lashmanov [2018] 2021) ):
  -                    `346789ABCDEFGHJKLMNPQRTUVWXYabcdefghijkmnpqrtwxyz`
* Length:              20 characters
* Canonical syntax:    XXXX-XXXX-XXXX-XXXX-XXXX
* Case-sensitive

## Recommended Comparison Method

The `-` characters are used purely for the human readability reason. It must not be considered as a semantics part in Leismore ShortID. While doing ID comparison, it must be removed from the IDs.

## Chance of Collision

When 1,000 IDs are being generated per second, in order to have a 1% probability of at least one collision, **~358 thousand years** are needed, according to the calculation of [Nano ID CC](https://zelark.github.io/nano-id-cc) (Zhuravlёv n.d.)

## References

* Sitnik, Andrey. (2017) 2021. Nano ID. JavaScript. https://github.com/ai/nanoid.
* Lashmanov, Stanislav. (2018) 2021. Nanoid-Dictionary. JavaScript. https://github.com/CyberAP/nanoid-dictionary.
* Zhuravlёv, Aleksandr. n.d. Nano ID CC. Web. Accessed October 19, 2021. https://zelark.github.io/nano-id-cc.
