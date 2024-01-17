<script>
import axios from 'axios';

export default {
    data() {
        return {
            project: {},
        };
    },

    methods: {
        fetchProject() {
            const slug = this.$forceUpdate.params.slug;
            axios.get(`http://localhost:8000/api/projects/${slug}`).then((res) => {
                this.project = res.data;
            }).catch((error) => {
                console.error('Can\'t recover data from project', error);
            });
        },
    },

    created() {
        this.fetchProject();
    }
}
</script>