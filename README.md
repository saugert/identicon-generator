# Identicon Generator

## Description

Do you like Github identicons but don't like the one github autogenerated for you? Maybe you want a different pattern, a specific color or you want your identicon to be asymmetrical? Here is a solution!

## Installation

1. Clone this repository.
2. Install necessary dependencies with `npm install` command.
3. Modify `config.js` file according to your needs.
4. Run `npm start`.

## Configuration

This generator is easily configurable, all you need to do is change values in the `config.js` file.

### Values

`stringToHash` - string that will be hashed with sha256 algorithm. Leave empty if you want to generate different identicons.

`size` - width of a row and a column in the identicon. Its value must be in range from 1 to 16.

`width` - width of the result image in pixels.

`amount` - amount of identicons you want to generate.

`color` - color for rectangles in an identicon. Must be in hex format (e.g. `"#ea37c2"`). Leave empty if you want different color for each identicon.

`backgroundColor` - hex format color for identicon background.

`isVerticallySymmetrical` - boolean value. If set to `true`, the left part of an identicon will be symmetrical to the right part.

`isHorizontallySymmetrical` - boolean value. If set to `true`, the top part of an identicon will be symmetrical to the bottom part.

### Possible improvements

- SHA256 algorithm is used for hashing a string, so a hashed string contains 256 bits. This means that maximum size is 16. A longer hash is required for greater size (`size ** 2 <= amount of bits in hash`).
