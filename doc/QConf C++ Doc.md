=====
3

4
## C Interface
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
5
### **Environment initialisation and destroy functions.**
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
6

7
-------
8

9
### **qconf_init** 
10

11
`int qconf_init();`
12

@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
13
Description
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
14
> Initial qconf environment
15
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
16
Parameters
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
17

@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
18
Return Value**
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
19

20
> QCONF_OK if success,  others if failed. 
21
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
22
Example
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
23
> int ret = qconf_init();
24
25
### **qconf_destroy**
26
`int qconf_destroy();`
27

@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
28
Description
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
29

30
>destroy qconf environment
31
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
32
Parameters
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
33

@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
34
Return Value
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
35

@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
36
Example
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
37
>qconf_destroy();
38
39
---
40

@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
41
### **QConf access functions wait version, retry sometime if configure not exist**
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
42

43
----
44

45
### **qconf_get_conf**
46

47
`int qconf_get_conf(const char *path, char *buf, unsigned int buf_len, const char *idc);`
48

@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
49
Description
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
50
>get configure value
51
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
52
Parameters
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
53
>path - key of configuration.
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
54
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
55
>buf - out parameter, buffer for value
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
56
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
57
>buf_len - lenghth of value buffer
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
58
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
59
>idc - from which idc to get the value，get from local idc if idc is NULL
60
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
61
Return Value
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
62
>QCONF_OK if success,  others if failed. QCONF_ERR_NOT_FOUND if configuration is not exists
63
 
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
64
Example 
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
65
>char value[QCONF_CONF_BUF_MAX_LEN];
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
66
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
67
>int ret = qconf_get_conf("demo/conf1", value, sizeof(value), NULL);
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
68
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
69
>assert(QCONF_OK == ret);   
70
71
### **qconf_get_batch_keys**
72

73
`int qconf_get_batch_keys(const char *path, string_vector_t *nodes, const char *idc);`
74

@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
75
Description
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
76
>get all children nodes'key
77
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
78
Parameters
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
79
>path - key of configuration.
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
80
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
81
>nodes - out parameter, keep all children nodes'key
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
82
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
83
>idc - from which idc to get the keys，get from local idc if idc is NULL
84
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
85
Return Value
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
86
>QCONF_OK if success,  others if failed. QCONF_ERR_NOT_FOUND if not exists
87
 
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
88
Example
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
89
>string_vector_t bnodes_key;
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
90
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
91
>init_string_vector(&bnodes_key);
92
> 
93
>int ret = qconf_get_batch_keys(path, &bnodes_key, NULL);
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
94
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
95
>assert(QCONF_OK == ret);
96
> 
97
>for (i = 0; i < bnodes_key.count; i++)
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
98
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
99
>{ cout << bnodes_key.data[i] << endl;}
100
> 
101
>destroy_string_vector(&bnodes_key); 
102
103

104
### **qconf_get_batch_conf**
105

106
`int qconf_get_batch_conf(const char *path, string_vector_t *nodes, const char *idc);`
107

@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
108
Description
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
109
>get all children nodes' key and value
110
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
111
Parameters
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
112
> path - key of configuration.
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
113
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
114
> nodes - out parameter, keep all children nodes' key and value
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
115
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
116
> idc - from which idc to get the children configurations，get from local idc if idc is NULL
117
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
118
Return Value
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
119
>QCONF_OK if success,  others if failed. QCONF_ERR_NOT_FOUND if not exists
120
 
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
121
Example
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
122
 >qconf_batch_nodes bnodes;
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
123
 >
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
124
 >init_qconf_batch_nodes(&bnodes);
125
 > 
126
 >int ret = qconf_get_batch_conf(path, &bnodes, NULL);
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
127
 >
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
128
 >assert(QCONF_OK == ret);
129
 > 
130
 >for (i = 0; i < bnodes.count; i++)
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
131
 >
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
132
 >{cout << bnodes.nodes[i].key << " : " << bnodes.nodes[i].value;}
133
 > 
134
 >destroy_qconf_batch_nodes(&bnodes); 
135
136
### **qconf_get_allhost**
137

138
`int qconf_get_allhost(const char *path, string_vector_t *nodes, const char *idc);`
139

@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
140
Description
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
141
>get all available services under given path
142
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
143
Parameters
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
144
 > path - key of configuration.
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
145
 >
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
146
 > nodes - out parameter, keep all available services
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
147
 >
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
148
 > idc - from which idc to get the services，get from local idc if idc is NULL
149
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
150
Return Value
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
151
>QCONF_OK if success,  others if failed. QCONF_ERR_NOT_FOUND if not exists
152
 
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
153
Example 
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
154
>string_vector_t nodes;
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
155
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
156
>init_string_vector(&nodes);
157
> 
158
>int ret = qconf_get_batch_conf(path, &nodes, NULL);
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
159
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
160
>assert(QCONF_OK == ret);
161
> 
162
>for (i = 0; i < nodes.count; i++)
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
163
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
164
>{cout << nodes.data[i] << endl;}
165
> 
166
>destroy_string_vector(&nodes_key); 
167
168
### **qconf_get_host**
169

170
`int qconf_get_host(const char *path, char *buf, unsigned int buf_len, const char *idc);`
171

@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
172
Description
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
173
>get one available service
174
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
175
Parameters
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
176
>path - key of configuration.
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
177
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
178
>buf - out parameter, keep the service
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
179
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
180
>buf_len - lenghth of buf
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
181
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
182
>idc - from which idc to get the value，get from local idc if idc is NULL
183
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
184
Return Value
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
185
>QCONF_OK if success,  others if failed. QCONF_ERR_NOT_FOUND if configuration is not exists
186
 
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
187
Example 
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
188
>char host[QCONF_HOST_BUF_MAX_LEN] = {0};
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
189
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
190
>int ret = qconf_get_host(path, host, sizeof(host), NULL);
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
191
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
192
>assert(QCONF_OK == ret);   
193
194
---
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
195
### **Data structure related functions**
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
196

197
----
198
``` c
199
typedef struct
200
  {
201
      int count;      // the number of services
202
      char **data;    // the array of services
203
  } string_vector_t;
204
```
205
### **init_string_vector**
206
207
`int init_string_vector(string_vector_t *nodes);`
208
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
209
Description
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
210
>initial array for keeping services
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
211
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
212
>**Tips:** the function should be called before calling qconf_get_batchkeys or qconf_get_allhosts
213
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
214
Parameters
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
215
>nodes - out parameter,  the array for keeping batch keys or services
216
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
217
Return Value
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
218
>QCONF_OK if success,  others if failed. QCONF_ERR_PARAM if nodes is null
219
 
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
220
Example 
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
221
>string_vector_t bnodes_key;
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
222
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
223
>init_string_vector(&bnodes_key);
224
225
### **destroy_string_vector**
226
227
`int destroy_string_vector(string_vector_t *nodes);`
228
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
229
Description
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
230
>destroy the array for keeping batch keys or services
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
231
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
232
>**Tips:** remember to call this function after the last use of string_vector_t
233
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
234
Parameters
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
235
>nodes - out parameter,  qconf_batch_nodes keeping batch keys or services
236
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
237
Return Value
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
238
>QCONF_OK if success,  others if failed. QCONF_ERR_PARAM if nodes is null
239
 
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
240
Example 
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
241
>qconf_batch_nodes nodes;
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
242
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
243
>destroy_string_vector(&nodes);
244
245
246
----
247
248
``` c
249
typedef struct qconf_node
250
  {
251
      char *key;
252
      char *value;
253
  } qconf_node;
254
255
  typedef struct qconf_batch_nodes
256
  {
257
      int count;
258
      qconf_node *nodes;
259
  } qconf_batch_nodes;
260
```
261
262
### **init_qconf_batch_nodes**
263
264
`int init_qconf_batch_nodes(qconf_batch_nodes *bnodes);`
265
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
266
Description
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
267
>initial nodes array for keeping batch conf
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
268
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
269
>**Tips:** the function should be called before calling qconf_get_batchconf
270
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
271
Parameters
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
272
>bnodes - out parameter,  qconf_batch_nodes to keeping batch nodes
273
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
274
Return Value
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
275
>QCONF_OK if success,  others if failed. QCONF_ERR_PARAM if nodes is null
276
 
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
277
Example 
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
278
>qconf_batch_nodes bnodes;
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
279
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
280
>init_qconf_batch_nodes(&bnodes);  
281
282
### **destroy_qconf_batch_nodes**
283
284
`int destroy_qconf_batch_nodes(qconf_batch_nodes *bnodes);`
285
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
286
Description
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
287
>destroy the nodes array for keeping batch conf
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
288
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
289
>**Tips:** remember to call this function after the last use of qconf_batch_nodes
290
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
291
Parameters
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
292
>bnodes - out parameter,  qconf_batch_nodes keeping batch nodes
293
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
294
Return Value
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
295
>QCONF_OK if success,  others if failed. QCONF_ERR_PARAM if nodes is null
296
 
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
297
Example
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
298
>qconf_batch_nodes bnodes;
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
299
>
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
300
>destroy_qconf_batch_nodes(&bnodes);
301
302
303
304
305
## Shell Command
306
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
307
### Usage:
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
308
309
``` c
310
qconf command key [idc]
311
command: can be one of below commands:
312
   get_conf        : get configure value
313
   get_host        : get one service
314
   get_allhost     : get all services available
315
   get_batch_keys  : get all children keys
316
   
317
key    : the path of your configure items
318
idc    : query from current idc if be omitted
319
```
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
320
### Example:
321
@haveTryTwo
1)Adding: Add QConf 1.0.0 : including agent which updates the share m…
3 years ago
322
``` shell
323
       qconf get_conf "demo/conf"
324
       qconf get_conf "demo/conf" "test"
325
       
326
       qconf get_host "demo/hosts"
327
       qconf get_host "demo/hosts" "test"
328
       
329
       qconf get_allhost "demo/hosts"
330
       qconf get_allhost "demo/hosts" "test"
331
332
	   qconf get_conf "demo/batch"
333
       qconf get_conf "demo/batch" "test"
@haveTryTwo
1)Changing: modify the README and c/c++, python, php document
3 years ago
334
```
© 2018 GitHub, Inc.