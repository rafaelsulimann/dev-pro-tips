```json

{
	// Place your snippets for java here. Each snippet is defined under a snippet name and has a prefix, body and
	// description. The prefix is what is used to trigger the snippet and the body will be expanded and inserted. Possible variables are:
	// $1, $2 for tab stops, $0 for the final cursor position, and ${1:label}, ${2:another} for placeholders. Placeholders with the
	// same ids are connected.
	// Example:
	"Rest Controller": {
		"prefix": "@rest",
		"body": [
			"@RestController",
			"@RequestMapping(value = Path.${1:PATH})"
		],
		"description": "Rest Controller Anotações"
	},
	"Entity": {
		"prefix": "@entity",
		"body": [
			"@Entity",
			"@Table(name = TableName.${1:TABELA})",
			"@Getter",
		],
		"description": "Entity Anotações"
	},
	"Id": {
		"prefix": "@id",
		"body": [
			"@Id",
    		"@GeneratedValue(strategy = GenerationType.${1:IDENTITY})"
		],
		"description": "Entity Anotações"
	},
	"Enum": {
		"prefix": "@enum",
		"body": [
			"@Enumerated(EnumType.${1:STRING})"
		],
		"description": "Enumerated Anotações"
	},
	"LocalDateTime Format": {
		"prefix": "@localdateformat",
		"body": [
			"@JsonFormat(shape = JsonFormat.Shape.STRING, pattern = \"yyyy-MM-dd'T'HH:mm:ss'Z'\")"
		],
		"description": "Local Date Time Anotações"
	},
	"Getter, Setter e Constructor": {
		"prefix": "@data",
		"body": [
			"@Getter",
		],
		"description": "Getter/Setter e construtores Anotações"
	},
	"ExistsById": {
		"prefix": "@existsById",
		"body": [
			"@ExistsById(domainClass = ${1:Entity}.class, fieldName = \"id\", message = \"${2:Entity} não encontrado\")"
		]
	},
	"SenhaLimpa": {
		"prefix": "@senhalimpa",
		"body": [
			"@SenhaLimpa(message = \"Senha não pode estar encodada\")"
		]
	},
	"ManyToOne": {
		"prefix": "@manyToOne",
		"body": [
			"@ManyToOne",
    		"@JoinColumn(name = \"${1:column_name}\")"
		]
	},
	"OneToOne": {
		"prefix": "@oneToOne",
		"body": [
			"@OneToOne(mappedBy=\"${1:refAttribute}\", cascade = CascadeType.ALL)",
		]
	},
	"OneToMany": {
		"prefix": "@oneToOne",
		"body": [
			"@OneToMany(mappedBy=\"${1:refAttribute}\")",
		]
	},
	"UniqueValue": {
		"prefix": "@uniqueValue",
		"body": [
			"@UniqueValue(domainClass = ${1:EntityName}.class, fieldName = \"${2:attributeName}\", message = \"${3:EntityName} já existente\")",
		]
	},
	"Size": {
		"prefix": "@size",
		"body": [
			"@Size(min = 6, message = \"${1:attribute} deve contêr no mínimo ${2:size} caracteres\")"
		]
	},
	"ValidEnum": {
		"prefix": "@validEnum",
		"body": [
			"@ValidEnum(enumClass = ${1:EntityName}.class, message = \"${2:EntityName} inválido\")",
		]
	},
	"NotBlank": {
		"prefix": "@notblank",
		"body": [
			"@NotBlank(message = ErrorMessage.CAMPO_OBRIGATORIO)",
		]
	},
	"NotNull": {
		"prefix": "@notnull",
		"body": [
			"@NotNull(message = ErrorMessage.CAMPO_OBRIGATORIO)",
		]
	},
	"Email": {
		"prefix": "@email",
		"body": [
			"@Email(message = \"Email inválido\")",
		]
	},
	"CPFOuCNPJ": {
		"prefix": "@cpforcnpj",
		"body": [
			"@CpfOrCnpj(message = \"Documento deve ser um CPF ou CNPJ\")",
		]
	},
	"Telefone": {
		"prefix": "@telefone",
		"body": [
			"@Telefone(message = \"Telefone precisa ter formato válido\")",
		]
	},
	"CEP": {
		"prefix": "@cep",
		"body": [
			"@Cep(message = \"CEP precisa ter formato válido\")",
		]
	},
	"JsonInclude.NON_NULL": {
		"prefix": "@jsonincludenonnull",
		"body": [
			"@JsonInclude(JsonInclude.Include.NON_NULL)",
		]
	},
	"AssertNotNull": {
		"prefix": "@assertnotnull",
		"body": [
			"Assert.notNull(${1:attribute}, \"${2:attributeName} não pode ser nulo\");",
		]
	},
	"AssertIsTrue": {
		"prefix": "@assertistrue",
		"body": [
			"Assert.isTrue(${1:attribute} != null && !${1:attribute}.isBlank(), \"${2:attributeName} não pode ser nulo ou em branco\");",
		]
	},
	"NoArgsConstructorDeprecated": {
		"prefix": "@noargsconstructordeprecated",
		"body": [
			"/**",
			"* @deprecated",
			"* Não utilizar! Criado por obrigação do hibernate",
			"*/",
			"@Deprecated"
		]
	},
	"PageableDefault": {
		"prefix": "@pageabledefault",
		"body": [
			"@PageableDefault(page = ${1:page}, size = ${2:size}, sort = \"userId\", direction = Sort.Direction.${3:direction})"
		]
	},
	"ManyToMany": {
		"prefix": "@manytomany",
		"body": [
			"@ManyToMany",
			"@JoinTable(name = \"${1:tableName}\", joinColumns = @JoinColumn(name = \"${2:classeAtualColumnName}\"), inverseJoinColumns = @JoinColumn(name = \"${3:outraClasseColumnName}\"))"
		]
	},
	"URI": {
		"prefix": "@uri",
		"body": [
			"ServletUriComponentsBuilder.fromCurrentRequest().path(\"/{id}\").buildAndExpand(${1:object}.getId()).toUri()"
		]
	},
}

```
