# php-imgfing

Create fingerprints of images to quickly find 
duplicates or very similar images. Uses GD or Imagick.

## Options

    bitSize     Bitsize of the fingerprint, multiple of 3, defaults to 300
    avgColor    Apply a correction based on the diff with the avg color, defaults to true
    adapters    Which adapters to use in this order. Defaults to ['Imagick', 'GD']
    

## Usage

    <?php
    $imgFing = new ImgFing([]);
    $f1 = $imgFing->identifyFile(__DIR__ . '/file.png');
    $f2 = $imgFing->identifyString(file_get_contents($uri));
    
    echo $imgFing->matchScore($f1, $f2);
    


