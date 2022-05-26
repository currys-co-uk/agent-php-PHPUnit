# ReportPortal agent for PHPUnit

PHPUnit agent for EPAM Report Portal

## How to use.

Use as an example: https://github.com/Mikalai-Kabzar/phpUnit-test-framework

### Steps:

#### 1) Add dependency to your composer.json file.
```
  "minimum-stability": "dev",
  "require-dev": {
    "reportportal/phpunit" : "*"
  },
```
Use as an example: https://github.com/Mikalai-Kabzar/phpUnit-test-framework/blob/master/composer.json

  
#### 2) Update phpunit.xml file with listener configuration.

```
    <listeners>
        <listener class="agentPHPUnit" file="vendor/reportportal/phpunit/src/agentPHPUnit.php">
            <arguments>
                <string>25667b03-8760-469f-ad41-fc0b9c4b67fa</string>
                <string>https://rp.epam.com</string>
                <string>mikalai_kabzar_personal</string>
                <string>.000+00:00</string>
                <string>test launch name !!!</string>
                <string>test launch description !!!</string>
                <array>
                    <element key="0">
                        <string>Name of env variable #1</string>
                    </element>
                    <element key="1">
                        <string>Name of env variable #2</string>
                    </element>
                </array>
            </arguments>
        </listener>
    </listeners> 
```
agentPHPUnit listener's variables description.

    - 1 - UUID.
    - 2 - Report Portal server URL.
    - 3 - Project name.
    - 4 - Time Zone.
    - 5 - Test Launch name.
    - 6 - Test launch description.
    - 7 - Array of environment variables names (optional)
    
Use as an example: https://github.com/Mikalai-Kabzar/phpUnit-test-framework/blob/master/phpunit.xml

#### 3) Fill in ```<string> ~ ~ ~ </string> ``` lines with data of your own Report Portal server.

#### 4) Run command "composer update" to get dependencies.

#### 5) Enjoy.
