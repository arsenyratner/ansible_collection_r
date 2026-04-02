# r.common.general

## Distribution specific

```yaml
- name: Distribution specific variables
  vars:
    distribution_firstfound_paths: ['vars']
  ansible.builtin.include_vars:
    file: "{{ lookup('ansible.builtin.first_found', distribution_firstfound) }}"

- name: Distribution specific tasks
  vars:
    distribution_firstfound_paths: ['tasks']
  ansible.builtin.include_tasks:
    file: "{{ lookup('ansible.builtin.first_found', distribution_firstfound) }}"
```
