# Configuration Properties @ConfigurationProperties (prefix)

Todas as suas estruturas dependem fortemente do application.properties

A proposta do Configuration Properties é ter um bean de configuração que todos os seus valores vem através do application.properties.


## Annotation Type ConfigurationProperties

@Target ( value ={ TYPE , METHOD })
  @Retention ( value = RUNTIME )
  @Documented 
  @Indexed 
public @interface ConfigurationProperties

Anotação para configuração externalizada. Adicione isso a uma definição de classe ou a um @Bean método em uma @Configuration classe se desejar vincular e validar algumas propriedades externas (por exemplo, de um arquivo .properties).
A vinculação é executada chamando setters na classe anotada ou, se @ConstructorBinding estiver em uso, vinculando-se aos parâmetros do construtor.

Observe que, ao contrário de @Value, as expressões SpEL não são avaliadas, pois os valores das propriedades são externalizados.