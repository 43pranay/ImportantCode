____________________________________________________________________________________________________________
|                                                                                                          |
|                                            Important Code                                                |
|__________________________________________________________________________________________________________|



===============================================================================================================

=> Parse SOAP Response

    private function decodeSOAPResponse($response='') {
      $response1 = preg_replace("/(<\/?)(\w+):([^>]*>)/", "$1$2$3", $response);
      $xml = simplexml_load_string($response1);
      $json = json_decode(json_encode($xml),true);
      return $json;
    }

===============================================================================================================

=> Random String Generator

    function generateRandomString($length = 10) {
        $characters = '0123456789abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ';
        $charactersLength = strlen($characters);
        $randomString = '';
        for ($i = 0; $i < $length; $i++) {
            $randomString .= $characters[rand(0, $charactersLength - 1)];
        }
        return $randomString;
    }

===============================================================================================================
