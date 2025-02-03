### This is an example of a basic chatbot app built using Java, with the following tools.

- Spring AI _and OpenAI ChatGPT service_
- Spring Boot (leveraging on autoconfigure)
- JDK 23 
> *Note* If you are using an earlier version of JDK, for example, 21, you may run into runtime problems possibly caused by incompatibilities among the Spring libraries and JDK.
>> In such case, first please update the version of Java in the pom.xml:
>> - \<java.version\>21\</java.version\>
>> 
>> Then, lower the version of your Spring web starter version to a version such as:
>> + \<artifactId\>spring-boot-starter-web\</artifactId\>
>>    + \<version>3.2.12\</version>
>

****
### To build it:

- `mvn clean install`

### To run it:

- `mvn spring-boot:run`


### To use the chatbot:

> The Spring AI project defines a configuration property names ***spring.ai.openai.api-key** that you need to set to the value of the OPENAI_API_KEY. The System Prerequisites file contains information on how you can obtain the API Key.
>> You can also set the following environment variable to use the value of your OPENAI_API_KEY, as follows:
> - SPRING_AI_OPENAI_API_KEY=\<YOUR_OPENAI_API_KEY\>

Run the curl command to see the result:
>`curl --get localhost:8080/ai/openai/chat`

##### Note: You can also use the HTTP client, like so:
> http://localhost:8080/ai/openai/chat'

---> To keep things simple here, notice that the question is hardcoded in the code (message='Tell me a joke').  Feel free to play around and change the question, and rebuild/rerun.
